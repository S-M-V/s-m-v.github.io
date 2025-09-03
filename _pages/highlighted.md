---
layout: default
title: "Highlighted Publications"
permalink: /highlighted/
author_profile: true
---

<h1>Highlighted Publications</h1>

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
      <li style="margin-bottom: 1.5em; padding-bottom: 1em; border-bottom: 1px dashed #ddd;">
        <p style="margin: 0;"><strong>{{ pub.title }}</strong></p>
        <p style="margin: 0.2em 0;"><em>{{ pub.venue }}</em>, {{ pub.date | date: "%B %Y" }}</p>

        {% if pub.excerpt %}
          <p style="margin: 0.5em 0; color: #555;">{{ pub.excerpt }}</p>
        {% endif %}

        {% if pub.paperurl %}
          <p style="margin: 0;">
            <a href="{{ pub.paperurl }}" target="_blank" style="color: #007acc;">🔗 View Paper</a>
          </p>
        {% endif %}

        {% if pub.citation %}
          <details style="margin-top: 0.5em;">
            <summary style="cursor: pointer;">📄 Citation</summary>
            <p style="font-size: 0.9em;">{{ pub.citation }}</p>
          </details>
        {% endif %}
      </li>
    {% endif %}
  {%- endfor -%}

  </ul>
{%- endfor -%}
