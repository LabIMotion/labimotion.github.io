---
layout: default
title: Archive
nav_order: 3
permalink: /blog/archive
---

{% assign page_files = site.pages | where_exp: "item", "item.path contains 'blog/categories/'" %}
{% assign filtered_pages = page_files | where_exp: "item", "item.name != 'index.md'" %}
{% assign actual_posts = filtered_pages | where_exp: "item", "item.path contains '/'" | where_exp: "item", "item.date" %}
{% assign sorted_posts = actual_posts | sort: 'date' | reverse %}

<div class="apple-hero-light" markdown="1">

# Archive

{{ sorted_posts | size }} posts, newest first.

</div>

{% for post in sorted_posts %}
  {% include post-preview.html post=post show_categories=true %}
{% endfor %}
