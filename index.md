---
layout: default
title: Quant Self Study
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

## HES Advanced Calc Notes
<ul>
  {% for note in site.hes %}
    <li>
      <a href="{{ note.url }}">{{ note.title }}</a>
      <small>— {{ note.date | date: "%b %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
[View all HES notes →](/hes/)

---

## Notebooks
<ul>
  {% assign nb = site.static_files | where_exp: "f", "f.extname == '.html' and f.path contains 'assets/notebooks'" %}
  {% for f in nb %}
    <li><a href="{{ f.path }}">{{ f.name }}</a></li>
  {% endfor %}
</ul>

---
