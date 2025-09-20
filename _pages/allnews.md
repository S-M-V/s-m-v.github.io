---
title: "SMV | News"
layout: textlay
excerpt: "SMV - News"
sitemap: false
permalink: /allnews.html
---

<h1>📰 News</h1>

<div class="news-container">
  {% assign sorted_news = site.data.news | sort: 'date' | reverse %}
  {% for article in sorted_news %}
    <div class="news-card">
      <div class="news-type">
        {% case article.type %}
          {% when "Event" %} 📢 Event
          {% when "Research" %} 🧪 Research
          {% when "Publication" %} 📚 Publication
          {% else %} 🔖 Other
        {% endcase %}
      </div>
      <div class="news-date">📅 {{ article.display_date | markdownify }}</div>
      <div class="news-headline">{{ article.headline | markdownify }}</div>
    </div>
  {% endfor %}
</div>
