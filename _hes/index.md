---
layout: default
title: "HES Notes"
permalink: /hes/
---

# HES Blog

<ul>
  {% for note in site.hes %}
    <li>
      <a href="{{ note.url }}">{{ note.title }}</a>
      <small>— {{ note.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
