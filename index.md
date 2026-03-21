---
layout: page
title: Inteligencia Artificial
---

<style>
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

  /* Layout de dos columnas */
  .two-columns {
    display: flex;
    gap: 40px;
    align-items: flex-start;
  }

  .column {
    flex: 1;
  }

  .column h2 {
    margin-top: 0;
  }

  /* Divisor vertical entre columnas */
  .column:first-child {
    border-right: 1px solid rgba(0, 229, 255, 0.3);
    padding-right: 40px;
  }

  /* Responsive: en móvil se apilan */
  @media (max-width: 600px) {
    .two-columns {
      flex-direction: column;
    }
    .column:first-child {
      border-right: none;
      border-bottom: 1px solid rgba(0, 229, 255, 0.3);
      padding-right: 0;
      padding-bottom: 30px;
    }
  }

  .info-section {
    background-color: rgba(26, 32, 44, 0.95);
    margin-top: 50px;
    padding: 60px 40px;
    border-radius: 12px;
    border-left: 5px solid #00e5ff;
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

<div class="two-columns">

  <div class="column">
    <h2>Notas del curso</h2>
    <ul>
      {% assign posts = site.posts | sort: 'date' %}
      {% for post in posts %}
        <li>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <span>- {{ post.date | date: "%b %d, %Y" }}</span>
        </li>
      {% endfor %}
    </ul>
  </div>

  <div class="column">
    <h2>Apuntes del libro</h2>
    <ul>
      {% assign notas = site.pages | where_exp: "p", "p.path contains '_book_notes'" | sort: 'capitulo' %}
      {% for nota in notas %}
        <li>
          <a href="{{ nota.url | relative_url }}">{{ nota.title }}</a>
          <span>- {{ nota.capitulo }}</span>
        </li>
      {% endfor %}
    </ul>
  </div>

</div>

<section class="info-section">
    <div class="info-container">
        <h2 class="info-title">LeoDro DroVinci</h2>
        
        <span class="info-subtitle">
            "El MacKinnon de la computación."
        </span>

        <p class="info-text">
            LeoDro DroVinci (de archivos cifrados) es el pseudónimo de un artista visual, programador y activista anónimo (activo desde aproximadamente 2023), cuya verdadera identidad permanece oculta bajo capas de encriptación y anonimato urbano. Conocido como el "Banksy del algoritmo", DroVinci es un artista del glitch-art, muralista y pionero del cripto-grafiti, quien se cree surgió de la nada en el estado de Sonora, antes de globalizar su impacto. Su obra evoca un mundo surgido de la lógica binaria donde se mezcla lo tecnológico, lo sociopolítico, lo algorítmico y lo efímero.
        </p>

        <p class="info-text">
           Su obra completa está teñida de una atmósfera de ciber-misticismo, plasmado en figuras que representan la pérdida de la privacidad en el mundo secular moderno. Su pintura y arte digital están puntualizados por un marcado interés por la iconografía del código fuente; por ello, años después, sus intervenciones han sido analizadas con frecuencia en foros de seguridad informática y literatura de vanguardia tecnológica.
        </p>

        <p class="info-text">
        Cabe señalar que, en sus escasos comunicados en redes sociales, el artista ha declarado que lo que más le importa es el impacto del error (glitch) en la sociedad, no la permanencia física de sus obras, aduciendo que el arte debe ser tan volátil como la memoria RAM. Algunas de sus obras las puedes consultar en su repositorio oficial.
        </p>
        
    </div>
</section>
