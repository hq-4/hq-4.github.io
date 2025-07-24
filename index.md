---
layout: default
title: A Blog
---

# Welcome to Self Study Blog

## Latest Blog Posts
<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
[View all posts →](/blog/)

---

## HES Notes


| Term | Course |
| -------- | ------- |
| 2025 Fall | Managerial Economics |


<ul>
  {% for note in site.hes %}
    <li>
      <a href="{{ note.url }}">{{ note.title }}</a>
      <small>— {{ note.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
[View all HES notes →](/hes/)


