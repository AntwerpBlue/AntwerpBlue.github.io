---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

# 👋 Welcome

I am **Zhaochen Wang**, interested in **quantitative research, market microstructure, and machine learning**. This site is being rebuilt as a compact research portfolio rather than a traditional academic homepage.

# 🎓 Education

Education details will be added here.

# 💼 Experience

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

# 🧪 Selected Projects

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

# 📝 Research Notes

{% assign recent_notes = site.notes | sort: "date" | reverse %}
{% if recent_notes.size > 0 %}
  <div class="content-card-list">
    {% for note in recent_notes limit: 3 %}
      <a class="content-card" href="{{ note.url | relative_url }}">
        <span class="content-card__header">
          <span class="content-card__title">{{ note.title }}</span>
          <span class="content-card__arrow" aria-hidden="true">→</span>
        </span>
        {% if note.date %}<span class="content-card__meta">{{ note.date | date: "%Y-%m-%d" }}</span>{% endif %}
        <span class="content-card__description">{{ note.excerpt | markdownify | strip_html | strip_newlines }}</span>
      </a>
    {% endfor %}
  </div>
{% else %}
  <p class="content-empty">No research notes have been published yet.</p>
{% endif %}

