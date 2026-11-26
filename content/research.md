---
title: 'Research'
date: 2022-10-24
type: landing

design:
  spacing: '5rem'

sections:
  - block: collection
    id: papers
    content:
      title: Featured Research
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 1

  - block: collection
    content:
      title: Publications & Presentations
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
---
