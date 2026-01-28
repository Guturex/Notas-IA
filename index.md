---
layout: page
title: Inteligencia Artificial
---

<style>
  body {
    /* Restauramos el fondo completo */
    background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("{{ '/assets/Ruffiatman.png' | relative_url }}") !important;
    background-size: cover !important;
    background-position: center !important;
    background-attachment: fixed !important;
    background-repeat: no-repeat !important;
    color: white !important;
  }

  /* Añadimos un contenedor semi-transparente para que el texto sea legible */
  .page-content {
    background: rgba(0, 0, 0, 0.6) !important; /* Capa oscura detrás del texto */
    padding: 30px !important;
    border-radius: 15px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
    margin-top: 20px;
  }

  /* Mejoramos la legibilidad de cada letra */
  h1, h2, h3, p, li, span {
    color: white !important;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.8) !important;
  }

  /* Enlaces con color cian brillante para que contrasten */
  a {
    color: #00e5ff !important;
    font-weight: bold;
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
    color: #ffffff !important;
  }

  /* Limpieza de fondos del tema original */
  .wrapper, .site-header, .site-footer {
    background: transparent !important;
    border: none !important;
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
