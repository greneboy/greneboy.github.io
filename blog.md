---
layout: default
title: Blog
prev: /
---
# Blog

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }} {{ post.tag }}</a>
    </li>
  {% endfor %}
</ul>
