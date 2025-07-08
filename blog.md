---
layout: default
title: Blog
prev: /
---
# Blog

{% for post in site.posts %}
{% assign currentdate = post.date | date: "%B %Y" %}
{% if currentdate != date %}
## {{ currentdate }}
{% assign date = currentdate %} 
{% endif %}
* <span class="gray">{{ post.date | date_to_string | date: "%d %a"}}</span> [{{ post.title }}]({{ post.url }})
{% endfor %}

