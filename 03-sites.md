---
layout:     default
title:      "Sites"
permalink:  /sites/
---

<div class="profileiner my-5">
  <div class="text-center mx-lg-auto mb-9">
    <h1 class="display-5 mb-4">Os melhores sites de finanças em um só lugar!</h1>
    <p class="lead">Investimos nosso tempo para que você possa investir melhor! <br>Encontre aqui os melhores aplicativos de finanças da atualidade.</p>
  </div>
</div>

<h3 class="display-6 mt-5 mb-4">Acompanhe o mercado</h3>
<div class="row row-cols-1 row-cols-lg-5 row-cols-md-3 g-3">
  {% for site in site.data.sites-mercado %}
  <div class="col d-flex">
    <div class="card card-body mb-2">
      <img class="rounded mb-3 foto shadow-sm" src="{{site.baseurl}}/assets/imgs/sites/{{ site.icon }}.jpg" alt="Ícone do site: {{ site.name }}">
      <h5 class="card-title mb-4">{{ site.name }}</h5>
      <p class="card-text">
        <a class="btn btn-primary" href="{{ site.url }}" target="_blank" role="button">
          <i class="fa-solid fa-arrow-up-right-from-square"></i> Site Oficial
        </a>
      </p>
    </div>
  </div>
  {% endfor %}
</div>