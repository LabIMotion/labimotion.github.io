---
layout: default
title: Blog
nav_order: 2
has_children: true
permalink: /blog
---

# LabIMotion Blog

{: .fw-500 }

## Latest Posts

{% assign page_files = site.pages | where_exp: "item", "item.path contains 'blog/categories/'" | where_exp: "item", "item.name != 'index.md'" %}

{% assign sorted_posts = page_files | sort: 'date' | reverse %}
{% for post in sorted_posts limit:3 %}
  <article class="post-preview mb-5">
    <h3>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    <time datetime="{{ post.date | date_to_xmlschema }}" class="fw-500">{{ post.date | date: "%B %d, %Y" }}</time>
    {% if post.categories %}
      <div class="post-categories mt-2">
        <span class="categories-label">Categories:</span>
        <span class="categories-container">
          {% for category in post.categories %}
            {% assign category_slug = category | strip | replace: " ", "-" | downcase %}
            <a href="{{ '/blog/categories/' | append: category_slug | relative_url }}" class="category-tag">{{ category }}</a>
          {% endfor %}
        </span>
      </div>
    {% endif %}
    {% if post.description %}
      <p class="mt-2">{{ post.description }}</p>
    {% endif %}
  </article>
{% endfor %}

[View All Posts](./archive) | [Browse by Category](./categories)
