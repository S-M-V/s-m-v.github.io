---
title: "SMV | News"
layout: textlay
excerpt: "SMV - News"
sitemap: false
permalink: /allnews.html
---

# News

{% assign sorted_news = site.data.news | sort: 'date' | reverse %}
{% for article in sorted_news %}
  <strong>{{ article.display_date }}</strong><br>
  {{ article.headline | markdownify }}
{% endfor %}
