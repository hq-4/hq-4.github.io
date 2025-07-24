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

## 🏷️ Tags

{% for tag in site.tags %}
<details markdown="1>
  <summary>{{ tag[0] }} ({{ tag[1].size }} posts)</summary>

  <ul>
    {% assign posts = tag[1] | sort: "date" | reverse %}
    {% for post in posts %}
      <li>
        <a href="{{ post.url }}">{{ post.date | date: "%b %-d" }} – {{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
</details>

{% endfor %}


## 📅 Timeline

{% assign posts_by_year = site.posts | group_by_exp: "p", "p.date | date: '%Y'" %}
{% for year in posts_by_year %}
<details markdown="1" {% if forloop.first %}open{% endif %}>
  <summary>{{ year.name }}</summary>

  {% assign sorted = year.items | sort: "date" | reverse %}
  {% for post in sorted %}
  - [{{ post.date | date: "%b %-d" }} – {{ post.title }}]({{ post.url }})
  {% endfor %}
</details>
{% endfor %}


