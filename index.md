---
layout: page
title: Inteligencia Artificial
---

<style>
  /* Mantenemos el resto de la página limpio */
  body {
    background-color: #ffffff !important;
    color: #333 !important;
  }

  /* Aplicamos el fondo de Ruffiatman solo al contenedor central */
  .page-content {
    background-image: url("{{ '/assets/Ruffiatman.png' | relative_url }}") !important;
    background-size: cover !important;
    background-position: center !important;
    background-repeat: no-repeat !important;
    
    /* Añadimos margen interno para que el texto no toque los bordes del dibujo */
    padding: 50px 20px !important;
    
    /* Forzamos que el texto en esta zona sea blanco para que sea legible */
    color: white !important;
    min-height: 60vh; /* Asegura que el área sea lo suficientemente alta */
  }

  /* Ajustamos los elementos internos para que resalten sobre el fondo oscuro */
  .page-content h2, .page-content li, .page-content span {
    color: white !important;
    text-shadow: 1px 1px 2px black; /* Sombra para mejorar legibilidad */
  }

  .page-content a {
    color: #00d4ff !important;
    font-weight: bold;
    text-decoration: underline;
  }

  /* Quitamos fondos blancos que el tema pone por defecto en el centro */
  .wrapper {
    background: transparent !important;
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
