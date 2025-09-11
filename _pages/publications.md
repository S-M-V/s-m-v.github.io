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
<!-- Google Scholar -->
{% if site.social.googlescholar %}
            <a href="{{ site.social.googlescholar }}" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar">
                <i class="ai ai-google-scholar" style="color:#4285F4;"></i>
              </a>
{% endif %}
<!-- ORCID -->
{% if site.social.orcid %}
            <a href="{{ site.social.orcid }}" target="_blank" rel="noopener noreferrer" aria-label="ORCID">
            <i class="ai ai-orcid" style="font-size:28px; color:#A6CE39;"></i>
            </a>
{% endif %}
<!-- Clarivate (ResearcherID) -->
{% if site.social.clarivate %}
            <a href="{{ site.social.clarivate }}" target="_blank" rel="noopener noreferrer" aria-label="ResearcherID">
            <i class="ai ai-clarivate" style="font-size:28px; color:#004B9A;"></i>
            </a>
{% endif %}
<!-- Scopus -->
{% if site.social.scopus %}
            <a href="{{ site.social.scopus }}" target="_blank" rel="noopener noreferrer" aria-label="Scopus">
            <i class="ai ai-scopus" style="font-size:28px; color:#FF4203;"></i>
            </a>
{% endif %}
<!-- arXiv -->
{% if site.social.arxiv %}
            <a href="{{ site.social.arxiv }}" target="_blank" rel="noopener noreferrer" aria-label="arXiv">
            <i class="ai ai-arxiv" style="font-size:28px; color:#B31B1B;"></i>
            </a>
{% endif %}
<!-- ResearchGate -->
{% if site.social.researchgate %}
            <a href="{{ site.social.researchgate }}" target="_blank" rel="noopener noreferrer" aria-label="ResearchGate">
            <i class="ai ai-researchgate" style="font-size:28px; color:#00CCBB;"></i>
            </a>
{% endif %}


{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

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
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
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

{% for publi in sorted_publications %}
  {{ forloop.index }}. {{ publi.title }} <br />
  <em>{{ publi.authors }}</em><br />
  <a href="{{ publi.link.url }}">{{ publi.link.display }}</a><br /><br />
{% endfor %}

