---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      username: admin
      text: ""
    design:
      css_class: dark
      color:
      background:
        image:
          filename: stacked-peaks.svg
          size: cover
          position: center

  - block: collection
    id: reports
    content:
      title: Weekly reports
      count: 2
      filters:
        folders:
          - reports
        featured_only: true
    design:
      view: article-grid
      columns: 2

  - block: collection
    id: modules
    content:
      title: Modules
      filters:
        folders:
          - modules
        featured_only: true
    design:
      view: article-grid
      columns: 2
---
