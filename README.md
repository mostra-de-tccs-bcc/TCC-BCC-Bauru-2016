# TCC-BCC-Bauru-2016

Monografias e Apresentações dos formandos de Ciência da Computação da UNESP
Bauru do ano de 2016 http://mostra-de-tccs-bcc.github.io/TCC-BCC-Bauru-2016

# Contribuição

Para publicar o seu TCC siga o [:zap:Github flow:zap:](https://guides.github.com/introduction/flow/):

- Faça um [*Fork*](https://guides.github.com/activities/contributing-to-open-source/#contributing) :fork_and_knife:;
- Crie uma cópia do [`autor-exemplo`](autor-exemplo) e altere ele para que fique com sua :wink:	;
	- Adicione seus arquivos em uma :exclamation: pasta com seu **nome** :exclamation: (ela é usada no campo `autornick` para fazer os links):
		- `thesis-nome.pdf`
		- `presentation-nome.pdf`
	- Adicione um arquivo em `_posts` com nome de  [`2017-02-18-nome.md`](autor-exemplo/2017-02-18-autor.md) (:sparkles: ele é o que vai aparecer no site :sparkles:) seguindo o **"Modelo de post"** :point_down:;
- Faça um *pull-request* no [repo original](https://github.com/mostra-de-tccs-bcc/TCC-BCC-Bauru-2016);
- Por último :mortar_board: :mortar_board: :beer: :beer:

## Modelo de post

```markdown
---
layout: posts
title:  "Titulo do trabalho"
date:   2017-02-17 16:16:01 -0600
categories: trabalho
autornick: nome
autor: "Nome do Autor"
orientador: "Prof. Dr. Nome do Orientador"
github: https://github.com/autor/tcc
---
Resumo

Palavras-chave: Chave
```


# Executando o site localmente

**TL;DR:** Fiz funcionar depois de muita tentativa, fica aqui alguns dos passos e meu desejo de *boa sorte* para você.

Para executar localmente são softwares necessários são:

- Ruby (plataforma)
- jekyll (cms)
- [tema architect](https://github.com/pages-themes/architect)
- JEKYLL_GITHUB_TOKEN=<seu-token> (token para o tema architect)

Depois de instalados todas as dependencias executar na pasta do projeto `jekyll serve` com este resultado:

```
$ jekyll serve
Configuration file: D:/github/TCC-BCC-Bauru-2016/_config.yml
Configuration file: D:/github/TCC-BCC-Bauru-2016/_config.yml
            Source: D:/github/TCC-BCC-Bauru-2016
       Destination: D:/github/TCC-BCC-Bauru-2016/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 13.614 seconds.
  Please add the following to your Gemfile to avoid polling for changes:
    gem 'wdm', '>= 0.1.0' if Gem.win_platform?
 Auto-regeneration: enabled for 'D:/github/TCC-BCC-Bauru-2016'
Configuration file: D:/github/TCC-BCC-Bauru-2016/_config.yml
    Server address: http://127.0.0.1:4000/TCC-BCC-Bauru-2016/
  Server running... press ctrl-c to stop.
[2017-02-22 01:11:15] ERROR `/favicon.ico' not found.
```

## Passos aproximados para instalar as dependencias

:exclamation: **passos aproximados, sem testes, sem garantias** :exclamation:

No windows `power shell` como *administrador* foi executada a instalação do gerenciador de pacotes [*chocolatey*](https://chocolatey.org/install) e então o ruby:

```cmd
Set-ExecutionPolicy UNRESTRICTED
iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex
choco install ruby -version 2.2.4
choco install ruby2.devkit
```

Também foi instalado o [*ruby dev kit*](https://github.com/oneclick/rubyinstaller/wiki/Development-Kit):

```cmd
cd C:\tools\DevKit2
ruby dk.rb init
```

Depois disso executei no `bash` (na mesma pasta `C:\tools\DevKit2`):

```bash
260  ruby dk.rb install
262  ruby -v
263  gem install bundler
```

Na pasta do projeto:

```
266  bundle install
288  JEKYLL_GITHUB_TOKEN=<toke>
290  echo $JEKYLL_GITHUB_TOKEN
298  jekyll serve
```
