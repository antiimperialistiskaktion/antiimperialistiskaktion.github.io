---
layout: single
title: "All Posts"
permalink: /posts/
---

{% assign sorted_posts = site.posts | sort: 'date' | reverse %}
{% if sorted_posts.size > 0 %}
<ul>
  {% for post in sorted_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%B %d, %Y" }}
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No posts yet!</p>
{% endif %}