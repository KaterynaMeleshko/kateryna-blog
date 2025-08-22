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
      text_align: center

  - block: collection
    id: reports
    content:
      title: Weekly Reports
      title_size: 1.4rem
      text: ""
      count: 2
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
      title_size: 1.4rem
      text: ""
      count: 2
      filters:
        folders:
          - modules
        page_type: post
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

---
