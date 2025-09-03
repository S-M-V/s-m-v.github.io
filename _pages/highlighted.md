---
layout: default
title: "Highlighted Publications"
permalink: /highlighted/
author_profile: true
---

<h2>Highlighted Publications</h2>

{% assign highlighted_pubs = site.publications | where: "highlight", true | sort: "date" | reverse %}

{% assign years = "" | split: "," %}

{% for pub in highlighted_pubs %}
  {% assign year = pub.date | date: "%Y" %}
  {% unless years contains year %}
    {% assign years = years | push: year %}
  {% endunless %}
{% endfor %}

{% for year in years %}
  <h3 style="margin-top: 40px;">{{ year }}</h3>
  <ul style="list-style-type: none; padding-left: 0;">

  {% for pub in highlighted_pubs %}
    {% assign pub_year = pub.date | date: "%Y" %}
    {% if pub_year == year %}
      <li style="margin-bottom: 30px;">
        <strong>{{ pub.title }}</strong><br>
        <em>{{ pub.venue }}</em>, {{ pub.date | date: "%B %Y" }}<br>

        {% if pub.excerpt %}
          <p style="margin: 5px 0;">{{ pub.excerpt }}</p>
        {% endif %}

        {% if pub.paperurl %}
          <a href="{{ pub.paperurl }}" target="_blank">🔗 View Paper</a>
        {% endif %}

        {% if pub.citation %}
          <details>
            <summary>Citation</summary>
            <p>{{ pub.citation }}</p>
          </details>
        {% endif %}
      </li>
    {% endif %}
  {% endfor %}

  </ul>
{% endfor %}
