---
layout: archive
title: "Highlighted Publications"
permalink: /highlighted/
author_profile: true
---
{% assign highlighted_pubs = site.publications | where: "highlight", true %}

{% if highlighted_pubs.size > 0 %}
  {% for post in highlighted_pubs %}
    {% include archive-single.html %}
  {% endfor %}
{% else %}
  <p>No highlighted publications found yet.</p>
{% endif %}
