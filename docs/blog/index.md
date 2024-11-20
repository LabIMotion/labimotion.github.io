---
layout: default
title: Blog
nav_order: 99
has_children: true
has_toc: true
---

# LabIMotion Blog

## Latest Posts

{% assign sorted_posts = site.posts | sort: 'date' | reverse %}
{% for post in sorted_posts limit:5 %}
  <article class="post-preview">
    <h3>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
    {% if post.categories %}
    <div class="post-categories">
      Categories:
      {% for category in post.categories %}
        <span class="category-tag">{{ category }}</span>
      {% endfor %}
    </div>
    {% endif %}
    {% if post.description %}
      <p>{{ post.description }}</p>
    {% endif %}
  </article>
{% endfor %}

[View All Posts](./archive)
