---
title: "SMV - Publications"
layout: gridlay
excerpt: "SMV -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Research highlights

**At the end of this page, you can find the [full list of publications](#full-list-of-publications).** You can check as well in 
{% if site.social.googlescholar %}
  <a href="{{ site.social.googlescholar }}" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar" title="Google Scholar">
    <i class="ai ai-google-scholar" style="font-size: 28px; color:#4285F4; margin-right: 10px;"></i>
  </a>
{% endif %}
{% if site.social.orcid %}
  <a href="{{ site.social.orcid }}" target="_blank" rel="noopener noreferrer" aria-label="ORCID" title="ORCID">
    <i class="ai ai-orcid" style="font-size: 28px; color:#A6CE39; margin-right: 10px;"></i>
  </a>
{% endif %}
{% if site.social.clarivate %}
  <a href="{{ site.social.clarivate }}" target="_blank" rel="noopener noreferrer" aria-label="Clarivate" title="Clarivate">
    <i class="ai ai-clarivate" style="font-size: 28px; color:#004B9A; margin-right: 10px;"></i>
  </a>
{% endif %}
{% if site.social.scopus %}
  <a href="{{ site.social.scopus }}" target="_blank" rel="noopener noreferrer" aria-label="Scopus" title="Scopus">
    <i class="ai ai-scopus" style="font-size: 28px; color:#FF4203; margin-right: 10px;"></i>
  </a>
{% endif %}
{% if site.social.arxiv %}
  <a href="{{ site.social.arxiv }}" target="_blank" rel="noopener noreferrer" aria-label="arXiv" title="arXiv">
    <i class="ai ai-arxiv" style="font-size: 28px; color:#B31B1B; margin-right: 10px;"></i>
  </a>
{% endif %}
{% if site.social.researchgate %}
  <a href="{{ site.social.researchgate }}" target="_blank" rel="noopener noreferrer" aria-label="ResearchGate" title="ResearchGate">
    <i class="ai ai-researchgate" style="font-size: 28px; color:#00CCBB; margin-right: 10px;"></i>
  </a>
{% endif %}

{% assign number_printed = 0 %}
{% for publi in site.data.all_publications %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <div class="well">
    <pubtit>{{ publi.title }}</pubtit>
    <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
    <p>{{ publi.description }}</p>
    
    {% if publi.authors_highlight %}
      <p><em>{{ publi.authors_highlight }}</em></p>
    {% else %}
      <p><em>{{ publi.authors }}</em></p>
    {% endif %}
    
    <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
    <p class="text-danger"><strong>{{ publi.news1 }}</strong></p>
    <p>{{ publi.news2 }}</p>
  </div>
</div>


{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

## Full List of publications

{% assign sorted_publications = site.data.all_publications | sort: "date" | reverse %}
{% assign current_year = "" %}
{% assign counter = 0 %}

{% for publi in sorted_publications %}
  {% assign year = publi.date | date: "%Y" %}

  {% if year != current_year %}
  <h3>{{ year }}</h3>
  {% assign current_year = year %}
  {% endif %}

  {% assign counter = counter | plus: 1 %}
  {{ counter }}. <strong>{{ publi.title }}</strong><br />
  <em>{{ publi.authors }}</em><br />
  <a href="{{ publi.link.url }}">{{ publi.link.display }}</a><br />
{% endfor %}
