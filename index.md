---
layout: default
title: Home
---
# greneboy's site

## [> about](about)
* github: [greneboy](https://github.com/greneboy)

## [> blog](blog)

### Recents
{% for post in site.posts limit:4 %}
* <span class="gray">{{ post.date | date_to_string | date: "%Y %b %d"}}</span> [{{ post.title }}]({{ post.url }}) 
{% for tag in post.tags %} #{{ tag }} {% endfor %}
{% endfor %}
[and more...](blog.html)

## [> projects](https://github.com/greneboy?tab=repositories)
* ### [ddcutil-bh1750](https://github.com/greneboy/ddcutil-bh1750)
A simple ddcutil daemon that automatically adjust your monitor DDC/CI over I²C brightness using ddcutil according to the lux data from the arduino serial.
![Image](https://raw.githubusercontent.com/greneboy/ddcutil-bh1750/main/bh1750.jpg)

## > contact
Can't do that yet.