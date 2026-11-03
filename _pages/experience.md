---
layout: default
title: "Experience"
permalink: /experience/
author_profile: true
---

<h1 class="page__title">Experience</h1>

<p class="page-lead">Research and engineering experience across quantitative modeling, high-frequency data, and production research systems. Select an entry to open its details.</p>

{% assign experience_items = site.experiences | sort: "order" %}
<div class="content-card-list">
  {% for item in experience_items %}
    <a class="content-card" href="{{ item.url | relative_url }}">
      <span class="content-card__header">
        <span class="content-card__title">{{ item.title }}</span>
        <span class="content-card__arrow" aria-hidden="true">→</span>
      </span>
      {% if item.organization or item.period %}
        <span class="content-card__meta">{{ item.organization }}{% if item.organization and item.period %} · {% endif %}{{ item.period }}</span>
      {% endif %}
      <span class="content-card__description">{{ item.summary }}</span>
    </a>
  {% endfor %}
</div>
