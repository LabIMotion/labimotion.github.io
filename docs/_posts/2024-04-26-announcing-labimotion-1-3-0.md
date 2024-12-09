---
layout: default
title: "LabIMotion 1.3.0 Release Announcement"
date: 2024-04-26
author: "Claire Lin"
parent: Blog
categories: [Announcements, Releases]
description: "LabIMotion 1.3.0 brings new features including Generic Element Reporting, Split Function, and Export/Import Collection capabilities"
---

# LabIMotion 1.3.0 is here! 🥁
{: .fw-500 }

<span class="fs-3">{{ page.description }}<span>

<span class="fw-500">{{ page.author }}</span><span class="mx-2 fw-500">·</span><time datetime="{{ page.date | date_to_xmlschema }}" class="fw-500">{{ page.date | date: "%B %d, %Y" }}</time>

<hr style="border-top: 1px solid #0d6efd;">

The open source LabIMotion project just released LabIMotion 1.3.0 with features and bug fixes.

## Highlights from LabIMotion 1.3.0

To celebrate this most recent release, here are the key features introduced in this release:

* As a User

  * **Generic Element Reporting Function** ([doc](https://www.chemotion.net/docs/labimotion/guides/user/elements/report))
  * **Generic Element Split Function** ([doc](https://www.chemotion.net/docs/labimotion/guides/user/elements/copy-split))
  * **Export/Import Collection function** ([doc](https://www.chemotion.net/docs/labimotion/guides/user/elements/export-import))

* As a Designer
  * **Restriction Setting** ([doc](https://www.chemotion.net/docs/labimotion/guides/designer/components/layers/restriction-setting))
  * **System Units and Customize Default Unit for Field** ([doc](https://www.chemotion.net/docs/labimotion/guides/designer/components/fields/types/system-defined))

For more detailed information, please refer to the release notes for [1.3.0](https://github.com/LabIMotion/labimotion/releases/tag/v1.3.0). Stay up-to-date with the latest developments by subscribing to our [mailing list](https://www.lists.kit.edu/sympa/subscribe/labimotion-users) to receive the latest updates.

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

