---
layout: default
title: Categories
parent: Blog
nav_order: 2
---

# Categories

{% assign categories = site.posts | map: "categories" | flatten | uniq | sort %}

{% for category in categories %}
<h2 id="{{ category | slugify }}">{{ category }}</h2>
<ul>
  {% assign category_posts = site.posts | where_exp: "post", "post.categories contains category" | sort: "date" | reverse %}
  {% for post in category_posts %}
    <li>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
{% endfor %}
