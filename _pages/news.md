---
layout: single
title: "News"
permalink: /news/
---

{% assign news_posts = site.news | sort: 'date' | reverse %}
{% if news_posts.size > 0 %}
<ul>
  {% for post in news_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%B %d, %Y" }}
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No news for now!</p>
{% endif %}
