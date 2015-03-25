---
layout: page
title: Gavin's Blog
tagline: Duang Duang的进步
---
{% include JB/setup %}
# 博客列表

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
