---
layout: page
title: Inteligencia Artificial
---

## Notas del curso

<ul>
  {% assign posts = site.posts | sort: 'date' %}
  {% for post in posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span>- {{ post.date | date: "%b %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
