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
          filename: backgroung.svg
          size: cover
          position: center
      text_align: center

  - block: collection
    id: reports
    content:
      title: Weekly Reports
      count: 2
      filters:
        folders:
          - reports
        featured_only: false
    design:
      view: card-grid  
      columns: 2
      card:
        shadow: true
        hover_effect: lift
        border_radius: "0.5rem"
        padding: "1rem"

  - block: collection
    id: modules
    content:
      title: Modules
      filters:
        folders:
          - modules
        featured_only: false
    design:
      view: card-grid
      columns: 2
      card:
        shadow: true
        hover_effect: lift
        border_radius: "0.5rem"
        padding: "1rem"
---
