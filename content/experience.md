---
title: 'Experience'
date: 2023-10-24
type: landing

design:
  spacing: '5rem'

# Note: `username` refers to the user's folder name in `content/authors/`

# Page sections
sections:
  - block: resume-experience
    content:
      username: me
    design:
      # Hugo date format
      date_format: 'January 2006'
      # Education or Experience section first?
      is_education_first: false
  - block: steps
    id: activity
    content:
      title: Activity
      subtitle: Academic & Professional Activities
      items:
        - title: Teaching Assistant
          text: "**2026** · KAIST — Teaching activities"

        - title: Research Presentation
          text: "**2025** · Academic conference presentation"

        - title: Academic Mentoring
          text: "**2024** · Mathematics and statistics mentoring"

    design:
      layout: timeline
      marker_style: dot
      connector: line

  - block: resume-skills
    content:
      title: Skills & Hobbies
      username: me
  - block: resume-awards
    content:
      title: Awards
      username: me
  - block: resume-languages
    content:
      title: Languages
      username: me
---
