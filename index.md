---
layout: page
title: Inteligencia Artificial
---

<style>
  /* 1. Aplicamos el fondo y el oscurecimiento a TODA la página */
  body {
    background-image: linear-gradient(rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0.75)), url("{{ '/assets/Ruffiatman.png' | relative_url }}") !important;
    background-size: cover !important;
    background-position: center !important;
    background-attachment: fixed !important;
    background-repeat: no-repeat !important;
    background-color: #000 !important; /* Fondo de respaldo negro */
    color: #f0f0f0 !important;
    margin: 0;
  }

  /* 2. Forzamos a que el encabezado y el pie de página sean transparentes o igual de oscuros */
  .site-header, .site-footer, .wrapper, .page-content {
    background: transparent !important;
    background-color: transparent !important;
    border: none !important;
    box-shadow: none !important;
  }

  /* 3. Estilo de los textos para que resalten en la oscuridad */
  h1, h2, h3, p, li, span, .site-title, .site-nav {
    color: #ffffff !important;
    text-shadow: 2px 2px 8px rgba(0, 0, 0, 1) !important;
  }

  /* 4. Enlaces con un color cian eléctrico para que se vean bien */
  a, .site-title {
    color: #00e5ff !important;
    text-decoration: none !important;
  }

  a:hover {
    color: #ffffff !important;
    text-shadow: 0 0 10px #00e5ff !important;
  }

  /* Ajuste para que la lista de notas se vea más limpia */
  ul {
    list-style-type: none;
    padding-left: 0;
  }
  
  li {
    margin-bottom: 15px;
    font-size: 1.1em;
  }
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
