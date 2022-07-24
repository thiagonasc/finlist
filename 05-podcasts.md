---
layout:     default
title:      "PodCasts"
description: "Os melhores podcasts de finanças e investimentos em um só lugar!"
permalink:  /podcasts/
---

<div class="profileiner my-5">
  <div class="text-center mx-lg-auto mb-9">
    <h1 class="display-5 mb-4">Os melhores podcasts de finanças e investimentos em um só lugar!</h1>
    <p class="lead">Investimos nosso tempo para que você possa investir melhor! <br>Encontre aqui os melhores aplicativos de finanças da atualidade.</p>
  </div>
</div>

<h3 class="display-6 mt-5 mb-4">Finanças e Investimentos</h3>
<div class="row row-cols-1 row-cols-lg-5 row-cols-md-3 g-3">
  {% for podcast in site.data.podcasts %}
  <div class="col d-flex">
    <div class="card card-body mb-2">
      <img class="rounded mb-3 foto shadow-sm" src="{{site.baseurl}}/assets/imgs/podcasts/{{ podcast.img }}.jpg" alt="Ícone do app {{ podcast.name }}">
      <h5 class="card-title mb-4">{{ podcast.name }}<br><small class="text-muted">{{ podcast.subtitle }}</small></h5>
      <p class="card-text">
        <a class="btn btn-primary stretched-link" href="{{ podcast.spotify }}" target="_blank" role="button">
          <i class="fa-brands fa-spotify"></i> Spotify
        </a>
      </p>
    </div>
  </div>
  {% endfor %}
</div>