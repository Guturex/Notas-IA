---
layout: page
title: Inteligencia Artificial
---

<style>
  body {
    background-image: url("{{ '/assets/Ruffiatman.png' | relative_url }}") !important;
    background-size: cover !important;
    background-position: center !important;
    background-attachment: fixed !important;
    background-repeat: no-repeat !important;
    color: white !important; /* Para que el texto sea legible sobre el fondo oscuro */
  }
  
  /* Esto hace que las cajas blancas del tema sean transparentes */
  .wrapper, .site-header, .site-footer, .page-content, .post-list-heading {
    background: none !important;
    background-color: transparent !important;
    border: none !important;
  }

  /* Color de los enlaces para que resalten */
  a { color: #00d4ff !important; }
  h1, h2, h3, p, span, li { color: white !important; }
</style>

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
