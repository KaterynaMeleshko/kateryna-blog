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
      background:
        color: red
        image:
          filename: stacked-peaks.svg
          size: cover
          position: center

  - block: markdown
    content:
      title: 'Purpose of this blog'
      subtitle: ''
      text: |-
        This blog will be used for weekly reports to track progress and self-reflection, as well as for documenting modules and related work.
    design:
      columns: '1'

  - block: collection
    id: reports
    content:
      title: Weekly reports
      count: 2
      order: desc
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
