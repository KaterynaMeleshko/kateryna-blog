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
      text_align: center

  - block: collection
    id: reports
    content:
      title: Weekly Reports
      text: "Explore all weekly reports with summaries and details."
      count: 4
      filters:
        folders:
          - reports
        featured_only: false
      link:
        text: "View all reports →"
        url: "reports/"
    design:
      view: card-grid
      columns: 2
      align: center
      card:
        style: shadow
        border: true
        padding: "1.5rem"
        title: true
        subtitle: true
        text: true
        image: true
        button: true

  - block: collection
    id: modules
    content:
      title: Modules
      text: "Browse available modules with guides and materials."
      count: 4
      filters:
        folders:
          - modules
        featured_only: false
      link:
        text: "View all modules →"
        url: "modules/"
    design:
      view: card-grid
      columns: 2
      align: center
      card:
        style: shadow
        border: true
        padding: "1.5rem"
        title: true
        subtitle: true
        text: true
        image: true
        button: true
