---
layout:     default-subnav
title:      "Corretoras"
description:  "As melhores corretoras de investimentos em um só lugar!"
permalink:  /corretoras/
---

<div class="profileiner my-5">
  <div class="text-center mx-lg-auto mb-9">
    <h1 class="display-5 mb-4">As melhores corretoras em um só lugar!</h1>
    <p class="lead">Investimos nosso tempo para que você possa investir melhor! <br>Encontre aqui os melhores aplicativos de finanças da atualidade.</p>
  </div>
</div>

<h3 class="display-6 mt-5 mb-4"><a id="nacional"></a>Nacional</h3>
<div class="row row-cols-1 row-cols-lg-5 row-cols-md-3 g-3">
  {% for corretora in site.data.corretoras %}
  {% if corretora.categoria == "nacional" %}
  <div class="col d-flex">
    <div class="card card-body mb-2">
      <img class="rounded mb-3 foto shadow-sm" src="{{corretora.baseurl}}/assets/imgs/corretoras/{{ corretora.logo }}.jpg" alt="Ícone do site: {{ corretora.name }}">
      <h5 class="card-title mb-4">{{ corretora.name }}</h5>
      <p class="card-text">
        <a class="btn btn-primary stretched-link" href="{{ corretora.url }}" target="_blank" role="button">
          <i class="fa-solid fa-arrow-up-right-from-square"></i> Site Oficial
        </a>
      </p>
    </div>
  </div>
  {% endif %}
  {% endfor %}
</div>

<h3 class="display-6 mt-5 mb-4"><a id="internacional"></a>Internacional</h3>
<div class="row row-cols-1 row-cols-lg-5 row-cols-md-3 g-3">
  {% for corretora in site.data.corretoras %}
  {% if corretora.categoria == "internacional" %}
  <div class="col d-flex">
    <div class="card card-body mb-2">
      <img class="rounded mb-3 foto shadow-sm" src="{{corretora.baseurl}}/assets/imgs/corretoras/{{ corretora.logo }}.jpg" alt="Ícone do site: {{ corretora.name }}">
      <h5 class="card-title mb-4">{{ corretora.name }}</h5>
      <p class="card-text">
        <a class="btn btn-primary stretched-link" href="{{ corretora.url }}" target="_blank" role="button">
          <i class="fa-solid fa-arrow-up-right-from-square"></i> Site Oficial
        </a>
      </p>
    </div>
  </div>
  {% endif %}
  {% endfor %}
</div>

<h3 class="display-6 mt-5 mb-4"><a id="criptomoedas"></a>Criptomoedas</h3>
<div class="row row-cols-1 row-cols-lg-5 row-cols-md-3 g-3">
  {% for corretora in site.data.corretoras %}
  {% if corretora.categoria == "criptomoedas" %}
  <div class="col d-flex">
    <div class="card card-body mb-2">
      <img class="rounded mb-3 foto shadow-sm" src="{{corretora.baseurl}}/assets/imgs/corretoras/{{ corretora.logo }}.jpg" alt="Ícone do site: {{ corretora.name }}">
      <h5 class="card-title mb-4">{{ corretora.name }}</h5>
      <p class="card-text">
        <a class="btn btn-primary stretched-link" href="{{ corretora.url }}" target="_blank" role="button">
          <i class="fa-solid fa-arrow-up-right-from-square"></i> Site Oficial
        </a>
      </p>
    </div>
  </div>
  {% endif %}
  {% endfor %}
</div>