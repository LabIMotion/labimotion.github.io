---
layout: default
title: Archive
parent: Blog
---

# Blog Archive

{% for post in site.posts %}
  <article class="post-preview">
    <h3>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
    {% if post.categories %}
    <span class="post-categories">
      Categories: {{ post.categories | join: ", " }}
    </span>
    {% endif %}
    {% if post.description %}
      <p>{{ post.description }}</p>
    {% endif %}
  </article>
{% endfor %}
