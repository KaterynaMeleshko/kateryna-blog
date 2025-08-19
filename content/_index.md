---
title: ""
date: 2022-10-24
type: landing

design:
  spacing: "3rem"
  font_family: "Helvetica, Arial, sans-serif"
  font_size: "1rem"

sections:
  - block: resume-biography-3
    content:
      username: admin
      text: ""
    design:
      css_class: dark
      color: red
      background:
        image:
          filename: background.jpg
          size: cover
          position: center
      align: center

  - block: collection
    id: reports
    content:
      title: Weekly reports
      count: 2
      filters:
        folders:
          - reports
        featured_only: false
      link:
        text: "View all reports →"
        url: "reports/"
    design:
      view: article-grid
      columns: 2
      align: center
      card:
        style: shadow
        border: true
        padding: "1rem"

  - block: collection
    id: modules
    content:
      title: Modules
      count: 2
      filters:
        folders:
          - modules
        featured_only: false
      link:
        text: "View all modules →"
        url: "modules/"
    design:
      view: article-grid
      columns: 2
      align: center
      card:
        style: shadow
        border: true
        padding: "1rem"

---