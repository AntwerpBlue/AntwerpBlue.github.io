---
layout: default
title: "Projects"
permalink: /projects/
author_profile: true
---

<h1 class="page__title">Projects</h1>

<p class="page-lead">Selected research and engineering work. Select a project to open its dedicated detail page.</p>

{% assign project_items = site.projects | sort: "order" %}
<div class="content-card-list">
  {% for item in project_items %}
    <a class="content-card" href="{{ item.url | relative_url }}">
      <span class="content-card__header">
        <span class="content-card__title">{{ item.title }}</span>
        <span class="content-card__arrow" aria-hidden="true">→</span>
      </span>
      <span class="content-card__description">{{ item.summary }}</span>
    </a>
  {% endfor %}
</div>
