---
title: "News"
layout: textlay
excerpt: "Spins & Materials Vanguard"
sitemap: false
permalink: /allnews.html
---

# News
{% assign sorted_news = site.data.news | sort: 'date' | reverse %}
{% for article in site.data.news %}
<p><strong>{{ article.date }}</strong><br>
  {{ article.headline | markdownify}}</p>
{% endfor %}
