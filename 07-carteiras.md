---
layout:     default
description: "As carteiras de investidores relevantes reunidas em um só lugar!"
title:      "Carteiras"
permalink:  /carteiras/
---

<div class="profileiner my-5">
    <div class="text-center mx-lg-auto mb-9">
    <h1 class="display-5 mb-4">{{ page.description }}</h1>
        <p class="lead">Investimos nosso tempo para que você possa investir melhor! <br>Encontre aqui as carteiras de investimentos de influencers da atualidade.</p>
    </div>
</div>

<h3 class="display-6 mt-5 mb-4">Carteiras</h3>

{% for carteira in site.data.carteiras %}
<div class="row">
	<div class="col-lg-2">
		<div class="card card-body border-light mb-4">
			<img class="rounded-circle" width="84" height="84" src="{{site.baseurl}}/assets/imgs/influenciadores/{{ carteira.instagram }}.jpg" alt="Imagem de perfil - {{ influenciador.name }}"><br>
			<h4>{{ carteira.responsavel }}</h4>
			<p>{{ carteira.titulo }}</p>
			<a class="btn btn-outline-primary stretched-link" href="http://www.instagram.com/{{ carteira.instagram }}" target="_blank" role="button"><i class="fab fa-instagram fa-lg"></i> Instagram</a>
		</div>
	</div>
	<div class= "col">
		<div class="card">
			<div class="card-body">
				<h5>Ações</h5>
		<table class="table table-sm table-hover">
			<thead>
				<tr class="table-light">
					<th scope="col">Ticker</th>
					<th scope="col">Segmento</th>
					<th class="text-end" scope="col">% em ações</th>
					<th class="text-end" scope="col">% em carteira</th>
				</tr>
			</thead>
			<tbody>
				{% for acao in carteira.acoes %}
				<tr>
					<th scope="row">{{ acao.ticker }}</th>
					<td>{{ acao.segmento }}</td>
					<td class="text-end" >{{ acao.percentualClasse }} %</td>
					<td class="text-end" >{{ acao.percentualCarteira }} %</td>
				</tr>
				{% endfor %}
			</tbody>
		</table>
		<br>
		<h5>Fundos Imobiliários</h5>
		<table class="table table-sm table-hover">
			<thead>
				<tr class="table-light">
					<th scope="col">Ticker</th>
					<th scope="col">Setor</th>
					<th scope="col" class="text-end">% em ações</th>
					<th scope="col" class="text-end">% em carteira</th>
				</tr>
			</thead>
			<tbody>
				{% for fii in carteira.fiis %}
				<tr>
					<th scope="row">{{ fii.ticker }}</th>
					<td>{{ fii.setor }}</td>
					<td class="text-end" >{{ fii.percentualClasse }} %</td>
					<td class="text-end" >{{ fii.percentualCarteira }} %</td>
				</tr>
				{% endfor %}
			</tbody>
		</table>
			</div>
			<div class="card-footer text-muted text-sm fst-italic">
				<div class="d-flex flex-row justify-content-between">
					<span>Fonte: {{ carteira.fonte }}</span>
					<span>Última atualização: {{ carteira.atualizacao }}</span>
				</div>
			</div>
		</div>
	</div>
</div>
{% endfor %}