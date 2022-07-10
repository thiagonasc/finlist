---
layout:     default
title:      "Influenciadores"
permalink:  /influenciadores/
---

<div class="profileiner my-5">
  <div class="text-center mx-lg-auto mb-9">
    <h1 class="display-5 mb-4">Os maiores influenciadores de finanças em um só lugar!</h1>
    <p class="lead">Investimos nosso tempo para que você possa investir melhor! <br>Encontre aqui os maiores influenciadores digitais de finanças da atualidade no Instagram.</p>
  </div>
</div>

<!-- TOP 5 -->
<h3 class="display-6 mt-5 mb-4">Top 5 mais seguidos no Instagram</h3>
<div class="row row-cols-1 row-cols-md-5 g-3">
  {% for influenciador in site.data.influenciadores limit:5 %}
  <div class="col d-flex">
    <div class="card card-body">
      <img class="rounded-circle mb-3 foto" src="{{site.baseurl}}/assets/imgs/influenciadores/{{ influenciador.instagram.profile }}.jpg" alt="Imagem de perfil - {{ influenciador.name }}">
      <h5 class="card-title">{{ influenciador.name }} {{ influenciador.lastname }}</h5>
      <h6 class="card-subtitle mb-2 text-muted">@{{ influenciador.instagram.profile }}</h6>
      <p class="card-text">
        {%- if influenciador.instagram -%}
        <a class="btn btn-outline-primary stretched-link" href="http://www.instagram.com/{{ influenciador.instagram.profile }}" target="_blank" role="button">
          <i class="fab fa-instagram fa-lg"></i> Instagram
        </a>
        {%- endif -%}
      </p>
    </div>
  </div>
  {% endfor %}
</div>



<h3 class="display-6 mt-5 mb-4">Lista de influenciadores</h3>

<ul class="list-group">
{% assign pos = 1 %}
{% for influenciador in site.data.influenciadores limit:10 %}
  <li class="list-group-item d-flex flex-row gap-3 py-4 align-items-center">
    <h6 class="opacity-50">#{{ pos }}</h6>
    <img src="{{site.baseurl}}/assets/imgs/influenciadores/{{ influenciador.instagram.profile }}.jpg" alt="profile" width="48" height="48" class="rounded-circle flex-shrink-0" alt="Imagem de perfil - {{ influenciador.name }}">
    <div class="flex-fill">
      <h6 class="mb-0">{{ influenciador.name }} {{ influenciador.lastname }}</h6>
      <p class="mb-0 opacity-75">@{{ influenciador.instagram.profile }}</p>
    </div>
    <small class="lh-1 me-2 d-none d-sm-block"><b>{{ influenciador.instagram.followers }}</b><br>seguidores</small>
    <a class="btn btn-outline-primary stretched-link" href="http://www.instagram.com/{{ influenciador.instagram.profile }}" target="_blank" role="button"><i class="fab fa-instagram fa-lg"></i> Instagram</a>
  </li>
{% assign pos = pos | plus:1 %}
{% endfor %}
</ul>

<br><small class="text-muted">Última atualização: 09 de julho de 2022</small>