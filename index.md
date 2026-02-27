---
layout: page
title: Inteligencia Artificial
---

<style>
  /* 1. Estilos actuales de tu página */
  body {
    background-image: linear-gradient(rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0.75)), url("{{ '/assets/Ruffiatman.png' | relative_url }}") !important;
    background-size: cover !important;
    background-position: center !important;
    background-attachment: fixed !important;
    background-repeat: no-repeat !important;
    background-color: #000 !important;
    color: #f0f0f0 !important;
    margin: 0;
  }

  .site-header, .site-footer, .wrapper, .page-content {
    background: transparent !important;
    background-color: transparent !important;
    border: none !important;
    box-shadow: none !important;
  }

  h1, h2, h3, p, li, span, .site-title, .site-nav {
    color: #ffffff !important;
    text-shadow: 2px 2px 8px rgba(0, 0, 0, 1) !important;
  }

  a, .site-title {
    color: #00e5ff !important;
    text-decoration: none !important;
  }

  a:hover {
    color: #ffffff !important;
    text-shadow: 0 0 10px #00e5ff !important;
  }

  ul {
    list-style-type: none;
    padding-left: 0;
  }
  
  li {
    margin-bottom: 15px;
    font-size: 1.1em;
  }

  /* 2. NUEVOS ESTILOS para el apartado de información (Estilo Remedios Varo) */
  .info-section {
    background-color: rgba(26, 32, 44, 0.95); /* Color oscuro sólido para contrastar con el fondo general */
    margin-top: 50px;
    padding: 60px 40px;
    border-radius: 12px;
    border-left: 5px solid #00e5ff; /* Detalle de color cian */
  }

  .info-container {
    max-width: 800px;
    margin: 0 auto;
  }

  .info-title {
    font-size: 2.5rem !important;
    margin-bottom: 10px !important;
    border-bottom: 2px solid #ffffff;
    display: inline-block;
    padding-bottom: 5px;
  }

  .info-subtitle {
    font-size: 1.2rem !important;
    color: #cbd5e0 !important;
    font-style: italic;
    margin: 20px 0 !important;
    display: block;
  }

  .info-text {
    font-size: 1.1rem !important;
    line-height: 1.8 !important;
    text-align: justify;
    color: #e2e8f0 !important;
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

<section class="info-section">
    <div class="info-container">
        <h2 class="info-title">Sobre este Proyecto</h2>
        
        <span class="info-subtitle">
            "Explorando los fundamentos de la computación inteligente en la UNISON."
        </span>

        <p class="info-text">
            Este repositorio de notas fue creado por un estudiante de Ciencias de la Computación 
            para centralizar el conocimiento adquirido en la materia de <strong>Inteligencia Artificial</strong>. 
            Aquí se documentan algoritmos de búsqueda, técnicas de optimización y modelos de aprendizaje 
            que forman la base de la tecnología moderna.
        </p>

        <p class="info-text">
            Al igual que en la obra de Varo, la IA busca encontrar patrones en lo complejo, 
            mezclando la lógica matemática con la creatividad computacional para resolver 
            problemas del mundo real.
        </p>
    </div>
</section>
