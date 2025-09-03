---
layout: default
title: "Highlighted Publications"
permalink: /highlighted/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<h2>{Highlighted works}</h2><hr />
<div class="wordwrap">Highlighted works</div>
{% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}

<h1>Highlighted Publications</h1>
{% include base_path %}
{% assign highlighted_pubs = site.publications | where: "highlight", true | sort: "date" | reverse %}

{% assign years = "" | split: "," %}

{%- for pub in highlighted_pubs -%}
  {% assign year = pub.date | date: "%Y" %}
  {% unless years contains year %}
    {% assign years = years | push: year %}
  {% endunless %}
{%- endfor -%}

{%- for year in years -%}
  <h2 style="margin-top: 2em; font-size: 1.75em; border-bottom: 2px solid #ccc;">{{ year }}</h2>
  <ul style="list-style-type: none; padding-left: 0;">

  {%- for pub in highlighted_pubs -%}
    {% assign pub_year = pub.date | date: "%Y" %}
    {% if pub_year == year %}
       {% include archive-single.html %}
    {% endif %}
  {%- endfor -%}

  </ul>
{%- endfor -%}
