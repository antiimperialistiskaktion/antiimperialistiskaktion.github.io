---
layout: single
title: "Events"
permalink: /events/
---

{% assign event_posts = site.events | sort: 'date' | reverse %}
{% if event_posts.size > 0 %}
<ul>
  {% for post in event_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%B %d, %Y" }}
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No events for now!</p>
{% endif %}
