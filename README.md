# AntwerpBlue.github.io

Personal quantitative-research homepage built with Jekyll and adapted from the MIT-licensed [Amber-Homepage-Template](https://github.com/AmberHeart/Amber-Homepage-Template), Academic Pages, and Minimal Mistakes.

The site is deployed to GitHub Pages from the `master` branch via GitHub Actions.

Homepage content lives in `_pages/about.md`; experience details live in `_experiences/`, project details live in `_projects/`, and research notes live in `_notes/`. Their index pages live in `_pages/`. Site identity and profile links live in `_config.yml`.

## Publishing research notes

Add each note as a Markdown file in `_notes/`, preferably named `YYYY-MM-DD-short-title.md`:

```markdown
---
title: "Note title"
date: 2026-11-03
excerpt: "A short description shown on the notes page."
tags:
  - market microstructure
  - machine learning
---

Write the note here in Markdown.
```

Committed notes are published at `/notes/<filename>/` and appear automatically on `/notes/`, newest first.

