---
layout:     default
title:      "Aplicativos"
description:  "Os melhores aplicativos de finanças em um só lugar!"
permalink:  /aplicativos/
---

<div class="profileiner my-5">
  <div class="text-center mx-lg-auto mb-9">
    <h1 class="display-5 mb-4">Os melhores aplicativos de finanças em um só lugar!</h1>
    <p class="lead">Investimos nosso tempo para que você possa investir melhor! <br>Encontre aqui os melhores aplicativos de finanças da atualidade.</p>
  </div>
</div>

<h3 class="display-6 mt-5 mb-4">Controle de investimentos</h3>
<div class="row row-cols-1 row-cols-lg-5 row-cols-md-3 g-3">
  {% for app in site.data.apps-controle %}
  <div class="col d-flex">
    <div class="card card-body mb-2">
      <img class="rounded mb-3 foto shadow-sm" src="{{site.baseurl}}/assets/imgs/aplicativos/{{ app.icon }}.png" alt="Ícone do app {{ app.name }}">
      <h5 class="card-title mb-4">{{ app.name }}</h5>
      <p class="card-text">
        <a class="btn btn-primary" href="{{ app.site }}" target="_blank" role="button">
          <i class="fa-solid fa-arrow-up-right-from-square"></i> Site Oficial
        </a>
      </p>
      <p class="card-text">
        <a class="btn btn-sm btn-outline-primary" href="https://play.google.com/store/apps/details?id={{ app.googlePlay }}" target="_blank" role="button">
          <i class="fa-brands fa-google-play"></i> Google Play
        </a>
      </p>
      <p class="card-text">
        <a class="btn btn-sm btn-outline-primary" href="https://apps.apple.com/BR/app/id/{{ app.appleStore }}" target="_blank" role="button">
          <i class="fa-brands fa-apple"></i> Apple Store
        </a>
      </p>
    </div>
  </div>
  {% endfor %}
</div>