---
layout: default
title: Service Interruption Due to Technical Issues
date: 2024-12-13
author: "Claire Lin"
parent: Blog
categories: [Announcements]
description: "Service goes down due to technical issue"
---

# Service Interruption Due to Technical Issues
{: .fw-500 }

<span class="fs-3">{{ page.description }}<span>

<span class="fw-500">{{ page.author }}</span><span class="mx-2 fw-500">·</span><time datetime="{{ page.date | date_to_xmlschema }}">{{ page.date | date: "%B %d, %Y" }}</time>

<hr style="border-top: 1px solid #0d6efd;">

The service is currently inaccessible due to the deployment of a non-functional version of the ELN.

We're aware of this technical issue and are working to get things back to normal as quickly as possible. We apologize for any inconvenience.

---

{% if page.categories %}
  <div class="post-categories mt-6">
    Categories:&nbsp;&nbsp;
    {% for category in page.categories %}
      <a href="/blog/categories#{{ category | slugify }}" class="category-tag">{{ category }}</a>
    {% endfor %}
  </div>
{% endif %}

---

### Subscribe & Share Feedback

Get the latest development updates, tips, and best practices, or share your feedback with us.

[<i class="bi bi-newspaper"></i> Subscribe](https://www.lists.kit.edu/sympa/subscribe/labimotion-users){: .btn .btn-blue }
[<i class="bi bi-envelope-at"></i> Email Us](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-blue }
