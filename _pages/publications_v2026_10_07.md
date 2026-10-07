---
title: "SMV | Publications"
layout: gridlay
excerpt: "SMV -- Publications."
sitemap: false
permalink: /publications/
---

<style>
.pub-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  margin: 20px 0 30px;
}
.pub-card {
  position: relative;
  display: flex;
  flex-direction: column;
  background: #fff;
  border: 1px solid #e3e3e3;
  border-radius: 6px;
  overflow: hidden;
  transition: box-shadow .15s ease, transform .15s ease;
}
.pub-card:hover {
  box-shadow: 0 4px 14px rgba(0, 0, 0, .12);
  transform: translateY(-2px);
}
.pub-card-img {
  height: 170px;
  padding: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-bottom: 1px solid #eee;
}
.pub-card-img img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}
.pub-card-body {
  display: flex;
  flex-direction: column;
  flex: 1;
  padding: 12px 14px 14px;
}
.pub-card-title {
  margin: 0 0 8px;
  font-size: 15px;
  font-weight: 600;
  line-height: 1.35;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
  overflow: hidden;
}
.pub-card-title a {
  color: inherit;
  text-decoration: none;
}
/* Makes the whole card clickable through the title link */
.pub-card-title a::after {
  content: "";
  position: absolute;
  top: 0; right: 0; bottom: 0; left: 0;
}
.pub-card-journal {
  margin: auto 0 0;
  font-size: 13px;
  color: #666;
}
/* Sits above the card-wide link so its own link stays clickable */
.pub-card-news {
  position: relative;
  z-index: 1;
  margin: 6px 0 0;
  font-size: 12px;
  font-weight: 600;
}
</style>

<h1>📚 Publications</h1>

---

<p>
  <a href="#full-list-of-publications"><strong>Full list of publications ↓</strong></a>
  &nbsp;·&nbsp; Also on&nbsp;
  <span style="display: inline-flex; gap: 10px; align-items: center;">
    {% if site.social.googlescholar %}
      <a href="{{ site.social.googlescholar }}" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar" title="Google Scholar" style="display: inline-block;">
        <i class="ai ai-google-scholar" style="font-size: 28px; color:#4285F4; vertical-align: middle;"></i>
      </a>
    {% endif %}
    {% if site.social.orcid %}
      <a href="{{ site.social.orcid }}" target="_blank" rel="noopener noreferrer" aria-label="ORCID" title="ORCID" style="display: inline-block;">
        <i class="ai ai-orcid" style="font-size: 28px; color:#A6CE39; vertical-align: middle;"></i>
      </a>
    {% endif %}
    {% if site.social.clarivate %}
      <a href="{{ site.social.clarivate }}" target="_blank" rel="noopener noreferrer" aria-label="Clarivate" title="Clarivate" style="display: inline-block;">
        <i class="ai ai-clarivate" style="font-size: 28px; color:#004B9A; vertical-align: middle;"></i>
      </a>
    {% endif %}
    {% if site.social.scopus %}
      <a href="{{ site.social.scopus }}" target="_blank" rel="noopener noreferrer" aria-label="Scopus" title="Scopus" style="display: inline-block;">
        <i class="ai ai-scopus" style="font-size: 28px; color:#FF4203; vertical-align: middle;"></i>
      </a>
    {% endif %}
    {% if site.social.arxiv %}
      <a href="{{ site.social.arxiv }}" target="_blank" rel="noopener noreferrer" aria-label="arXiv" title="arXiv" style="display: inline-block;">
        <i class="ai ai-arxiv" style="font-size: 28px; color:#B31B1B; vertical-align: middle;"></i>
      </a>
    {% endif %}
    {% if site.social.researchgate %}
      <a href="{{ site.social.researchgate }}" target="_blank" rel="noopener noreferrer" aria-label="ResearchGate" title="ResearchGate" style="display: inline-block;">
        <i class="ai ai-researchgate" style="font-size: 28px; color:#00CCBB; vertical-align: middle;"></i>
      </a>
    {% endif %}
  </span>
</p>

---

<h2>Research highlights</h2>

{% assign highlights = site.data.all_publications | where: "highlight", 1 %}
<div class="pub-grid">
{%- for publi in highlights %}
  <div class="pub-card">
    <div class="pub-card-img">
      <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" alt="" loading="lazy" />
    </div>
    <div class="pub-card-body">
      <p class="pub-card-title">
        <a href="{{ publi.link.url }}" target="_blank" rel="noopener noreferrer" title="{{ publi.title | escape }}">{{ publi.short_title | default: publi.title }}</a>
      </p>
      <p class="pub-card-journal">{{ publi.link.display }}</p>
      {%- if publi.news1 and publi.news1 != "" %}
      <p class="pub-card-news text-danger">{{ publi.news1 }}</p>
      {%- endif %}
    </div>
  </div>
{%- endfor %}
</div>

{% assign sorted_publications = site.data.all_publications | sort: "date" | reverse %}

---
<a id="full-list-of-publications"></a>
<h2>Full List of Publications</h2>

<small>
  This section includes both the 
  **<a href="#principal">Principal Publications</a>** and the 
  **<a href="#collaborative">Collaborative Publications</a>**.
</small>

<a id="principal"></a>
<h3>
  Principal Publications <small>(<span title="Corresponding Author">📧</span> = corresponding author, <span title="Equal Contribution">🤝</span> = equal contribution)</small>
</h3>

<ol>
{% for publi in sorted_publications %}
  {% if publi.principal_publication == 1 %}
    <li>
      <strong>{{ publi.title }}</strong><br />
      <em>{{ publi.authors_highlight }}</em><br />
      <a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
    </li>
  {% endif %}
{% endfor %}
</ol>

<a id="collaborative"></a>
<h3>Collaborative Publications</h3>
<ol start="{{ sorted_publications | where: 'principal_publication', 1 | size | plus: 1 }}">
{% for publi in sorted_publications %}
  {% if publi.principal_publication == 0 %}
    <li>
      <strong>{{ publi.title }}</strong><br />
      <em>{{ publi.authors }}</em><br />
      <a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
    </li>
  {% endif %}
{% endfor %}
</ol>
