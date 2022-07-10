---
layout:     default
title:      "Canais"
permalink:  /canais/
published:  false
---

<div>
  <h2 class="mt-4 mb-4">Vídeos destaques</h2>
</div>

<div class="row row-cols-1 row-cols-md-5 g-4">
  {% for canal in site.data.canais-youtube %}
  <div class="col d-flex">
    <div class="card">
      <a href="https://www.youtube.com/watch?v={{ canal.video.id }}" target="_blank" class="stretched-link"><img src="https://img.youtube.com/vi/{{ canal.video.id }}/0.jpg" class="card-img-top" alt="..."></a>
      <div class="card-body">
        <p class="card-text">{{ canal.video.titulo }}</p>
        <h5 class="card-title">{{ canal.nome }}</h5>
      </div>
    </div>
  </div>
  {% endfor %}
</div>

<div>
  <h2 class="mt-4 mb-4">Top 10</h2>
</div>


