---
title: "SMV | News"
layout: textlay
excerpt: "SMV - News"
sitemap: false
permalink: /allnews/
---

<h1>📰 News</h1>

<div class="news-container">
  {% assign sorted_news = site.data.news | sort: 'date' | reverse %}
  {% for article in sorted_news %}
    <div class="news-card {{ article.type | downcase }}">
      <div class="news-date">📅 <b>{{ article.display_date }}</b></div>
      <div class="news-headline">{{ article.headline }}</div>
    </div>
  {% endfor %}
</div>
