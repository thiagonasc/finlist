---
layout:     default
title:      "Livros"
description: "Os melhores livros de economia, finanças e investimentos em um só lugar!"
permalink:  /livros/
---

<div class="profileiner my-5">
  <div class="text-center mx-lg-auto mb-9">
    <h1 class="display-5 mb-4">{{ page.description }}</h1>
    <p class="lead">Investimos nosso tempo para que você possa investir melhor! <br>Encontre aqui os melhores aplicativos de finanças da atualidade.</p>
  </div>
</div>

<h3 class="display-6 mt-5 mb-4">Mais vendidos do ano</h3>

<div class="row row-cols-1 row-cols-lg-5 row-cols-md-3 g-3">
  {% for livro in site.data.livros %}
  <div class="col d-flex">
    <div class="card border-light card-body mb-2">
	  <img class="rounded mb-3 foto shadow-sm" src="//ws-na.amazon-adsystem.com/widgets/q?_encoding=UTF8&ASIN={{ livro.asin }}&Format=_SL160_&ID=AsinImage&MarketPlace=BR&ServiceVersion=20070822&WS=1&tag=finlist-20&language=pt_BR" alt="Capa do livro: {{ livro.name }}" />
      <h5 class="card-title mb-4">{{ livro.titulo }}<br><small class="text-muted">{{ livro.subtitulo }}</small></h5>
	  <p>Por: {{ livro.autor }}</p>
      <p class="card-text">
        <a class="btn btn-primary stretched-link" href="{{ livro.url }}" target="_blank" role="button">
          <i class="fa-brands fa-amazon"></i> Ver na Amazon
        </a>
      </p>
    </div>
  </div>
  {% endfor %}
</div>