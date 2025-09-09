---
layout: single
title: "News"
permalink: /news/
---

{% assign news_posts = site.news | sort: 'date' | reverse %}
{% if news_posts.size > 0 %}
<ul>
  {% for post in news_posts %}
    <li style="margin-bottom: 2em;">
      <a href="{{ post.url }}" style="font-weight:bold; font-size:1.1em;">{{ post.title }}</a>
      <br>
      <small>{{ post.date | date: "%B %d, %Y" }}</small>
      
      <div style="margin-top:0.5em;">
        {{ post.content | markdownify }}
      </div>
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No news for now!</p>
{% endif %}

