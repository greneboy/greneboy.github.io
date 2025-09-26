---
layout: sub-default
title: Blog
permalink: /blog/
description: "Mostly rants, sarcasm, jokes, rarely informative."
---
{{page.description}}

<!-- Html Elements for Search -->
<div id="search-container">
<input type="text" id="search-input" name="test" placeholder="search...">
<ul id="results-container"></ul>
</div>

<!-- Script pointing to search-script.js -->
<script src="{{ "/assets/js/search.js" | relative_url }}" type="text/javascript"></script>

<!-- Configuration -->
<script>
SimpleJekyllSearch({
  searchInput: document.getElementById('search-input'),
  resultsContainer: document.getElementById('results-container'),
  searchResultTemplate: '<li><a href="{url}">{title}</a><span class="gray"> {date}</span></div> tags: {tags}</li>',
  json: '/search.json'
})
</script>

{% for post in site.posts %}
{% assign currentdate = post.date | date: "%B %Y" %}
{% if currentdate != date %}
## {{ currentdate }}
{% assign date = currentdate %} 
{% endif %}
* ### [{{ post.title }}]({{ post.url }}) 
<span class="gray">{{ post.date | date_to_string | date: "%d %a"}}</span> · {{ post.description }} {% for tag in post.tags %} <span class="gray">#{{ tag }} {% endfor %}</span>
{% endfor %}

