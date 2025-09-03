---
layout: archive
title: "Highlighted Publications"
permalink: /highlighted/
author_profile: true
---

{% for post in site.publications %}
  {% if post.highlight == true %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
