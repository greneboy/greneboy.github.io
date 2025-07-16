---
layout: sub-default
title: Blog
prev: /
---
Mostly rants, sarcasm, jokes, rarely informative.

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
* <span class="gray">{{ post.date | date_to_string | date: "%d %a"}}</span> [{{ post.title }}]({{ post.url }}) · {% for tag in post.tags %} #{{ tag }} {% endfor %}
{% endfor %}

