---
title: "SMV | News"
layout: textlay
excerpt: "SMV - News"
sitemap: false
permalink: /allnews/
---

# 📰 News

<div class="news-container">

{% assign sorted_news = site.data.news | sort: 'date' | reverse %}
{% for article in sorted_news %}
<div class="news-card">
  <div class="news-date">📅 {{ article.display_date }}</div>
  <div class="news-headline">{{ article.headline | markdownify }}</div>
</div>
{% endfor %}

</div>
