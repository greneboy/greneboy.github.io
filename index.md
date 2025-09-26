---
layout: default
title: Home
description: "A personal site made by greneboy."
---

# greneboy's site
{{page.description}}

## [> about](about)
* github: [greneboy](https://github.com/greneboy)

## [> blog](blog)

### Recents
{% for post in site.posts limit:4 %}
* ### [{{ post.title }}]({{ post.url }})
<span class="gray">{{ post.date | date_to_string | date: "%Y %b %d"}}</span> · {{ post.description }} <span class="gray"> {% for tag in post.tags %} #{{ tag }}{% endfor %} </span>
{% endfor %}
[and more...](blog)

## [> project](project)
{% for post in site.project limit:4 %}
* ### [{{ post.title }}]({{ post.url }}) 
{{ post.description }} {% for tag in post.tags %} <span class="gray">#{{ tag }}</span> {% endfor %}
{% endfor %}
[and more...](project)

## > contact
Email me at <a href="mailto:me@greneboy.com">me@greneboy.com</a>