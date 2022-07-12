---
layout:     default
title:      "Aplicativos"
permalink:  /aplicativos/
---

<div class="profileiner my-5">
  <div class="text-center mx-lg-auto mb-9">
    <h1 class="display-5 mb-4">Os aplicativos de finanças em um só lugar!</h1>
    <p class="lead">Investimos nosso tempo para que você possa investir melhor! <br>Encontre aqui os melhores aplicativos de finanças da atualidade.</p>
  </div>
</div>

<!-- TOP 5 -->
<h3 class="display-6 mt-5 mb-4">Controle seus investimentos</h3>
<div class="row row-cols-1 row-cols-md-5 g-3">
  {% for app in site.data.aplicativos limit:5 %}
  <div class="col d-flex">
    <div class="card card-body">
      <img class="rounded mb-3 foto shadow-sm" src="{{site.baseurl}}/assets/imgs/aplicativos/{{ app.icon }}.png" alt="Ícone do app {{ app.name }}">
      <h5 class="card-title">{{ app.name }}</h5>
      <p class="card-text">
        <a class="btn btn-outline-primary stretched-link" href="{{ app.site }}" target="_blank" role="button">
          <i class="fa-solid fa-arrow-up-right-from-square"></i> Site Oficial
        </a>
      </p>
    </div>
  </div>
  {% endfor %}
</div>