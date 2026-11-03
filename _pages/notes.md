---
layout: default
title: "Research Notes"
permalink: /notes/
author_profile: true
---

<h1 class="page__title">Research Notes</h1>

<p class="notes-intro">Research notes, implementation details, and technical write-ups. New notes are published here in reverse chronological order.</p>

{% assign published_notes = site.notes | sort: "date" | reverse %}
{% if published_notes.size > 0 %}
  <ol class="notes-list">
    {% for note in published_notes %}
      <li class="notes-list__item">
        <article>
          <h2 class="notes-list__title"><a href="{{ note.url | relative_url }}">{{ note.title }}</a></h2>
          {% if note.date or note.tags or note.status %}
            <p class="notes-list__meta">
              {% if note.date %}<time datetime="{{ note.date | date_to_xmlschema }}">{{ note.date | date: "%Y-%m-%d" }}</time>{% endif %}
              {% if note.status == "template" %}<span class="notes-list__status">Template placeholder</span>{% endif %}
              {% if note.tags and note.tags.size > 0 %}<span class="notes-list__tags">{{ note.tags | join: " · " }}</span>{% endif %}
            </p>
          {% endif %}
          {% if note.excerpt %}<div class="notes-list__excerpt">{{ note.excerpt | markdownify }}</div>{% endif %}
        </article>
      </li>
    {% endfor %}
  </ol>
{% else %}
  <p class="notes-empty">No notes have been published yet. The first one will appear here automatically.</p>
{% endif %}
