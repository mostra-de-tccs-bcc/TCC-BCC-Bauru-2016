# Sobre a Mostra

Realizada anualmente, a Motra de TCCs de BCC tem por objetivo inspirar e
apresentar aos alunos, professores, funcionários e a comunidade (em especial as
empresas e desenvolvedores de software locais) as invoações e realizações
acadamicas consquistas e contruidas pelos alunos graduandos desta universidade.

# A Mostra 2016

A Mostra de Trabalhos de Conclusão de Curso (TCC) do curso de Bacharelado em
Ciência da Computação (BCC) da Faculdade de Ciências do Campus de Bauru será
realizada no dia 20/fev/2017 (segunda-feira), das 14 às 18h, no Hall Terra da
Fundeb.

# Trabalhos

<ul>
	{% for post in site.posts %}
	<li>
	<a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
	<p>Autor: {{ post.autor }} <br />
	Orientador: {{ post.orientador }}</p>
	</li>
	{% endfor %}
</ul>
