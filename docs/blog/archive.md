---
layout: default
title: Archive
parent: Blog
nav_order: 2
permalink: /blog/archive
---

# Blog Archive

All posts listed by date
{: .fs-6 .fw-300 }

{% assign page_files = site.pages | where_exp: "item", "item.path contains 'blog/categories/'" %}
{% assign filtered_pages = page_files | where_exp: "item", "item.name != 'index.md'" %}
{% assign actual_posts = filtered_pages | where_exp: "item", "item.path contains '/'" | where_exp: "item", "item.date" %}

{% assign sorted_posts = actual_posts | sort: 'date' | reverse %}

{% for post in sorted_posts %}
  <article class="post-preview mb-4">
    <h3>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    <time datetime="{{ post.date | date_to_xmlschema }}" class="fw-500">{{ post.date | date: "%B %d, %Y" }}</time>
    {% if post.categories %}
      {% include category-tags-only.html categories=post.categories %}
    {% endif %}
    {% if post.description %}
      <p class="mt-2">{{ post.description }}</p>
    {% endif %}
  </article>
{% endfor %}
