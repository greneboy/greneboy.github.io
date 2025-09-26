---
layout: sub-default
title: Project
permalink: /project
description: "Find around and find out."
---
{{page.description}}

{% for post in site.project %}
* ### [{{ post.title }}]({{ post.url }}) 
{{ post.description }} <span class="gray">{% for tag in post.tags %} #{{ tag }} {% endfor %}</span>
{% endfor %}