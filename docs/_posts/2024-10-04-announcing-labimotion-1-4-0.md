---
layout: default
title: "LabIMotion 1.4.0 Release Announcement"
date: 2024-10-04
author: "Claire Lin"
parent: Blog
categories: [Announcements, Releases]
description: "LabIMotion 1.4.0 brings new features including image previews, custom labeling, and interactive workflows"
---

# 🥁 Chemotion LabIMotion 1.4.0 is here!
{: .fw-500 }

<span class="fs-3">{{ page.description }}<span>

<span class="fw-500">{{ page.author }}</span><span class="mx-2 fw-500">·</span><time datetime="{{ page.date | date_to_xmlschema }}" class="fw-500">{{ page.date | date: "%B %d, %Y" }}</time>

<hr style="border-top: 1px solid #0d6efd;">

We are pleased to announce the release of LabIMotion 1.4.0! 🚀 Discover the exciting updates in our [1.4.0 release discussion](https://github.com/LabIMotion/labimotion/discussions/30) for all the details!

---

{% if page.categories %}
  <div class="post-categories mt-6">
    Categories:&nbsp;&nbsp;
    {% for category in page.categories %}
      <a href="./categories#{{ category | slugify }}" class="category-tag">{{ category }}</a>
    {% endfor %}
  </div>
{% endif %}

---

### Subscribe & Share Feedback

Get the latest development updates, tips, and best practices, or share your feedback with us.

[<i class="bi bi-newspaper"></i> Subscribe](https://www.lists.kit.edu/sympa/subscribe/labimotion-users){: .btn .btn-blue }
[<i class="bi bi-envelope-at"></i> Email Us](mailto:chemotion-labimotion@lists.kit.edu){: .btn .btn-blue }
