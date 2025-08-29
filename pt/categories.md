---
lang: pt
lang-niv: fonto
lang-ref: 003-jbk
layout: page
title: 'Categorias'
---

# Categorias do Blog

Navegue pelos artigos por categoria para encontrar o conteúdo que mais lhe interessa.

## Categorias Principais

- [Blog](/category/blog/) - Atualizações e pensamentos gerais
- [Projetos](/category/projects) - Mostra do meu trabalho
- [Tutoriais](/category/tutorials) - Guias passo a passo
- [Tecnologia](/category/technology) - Análises e resenhas tecnológicas
- [Desenvolvimento](/category/development) - Programação e tópicos de codificação

## Publicações Recentes

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%d/%m/%Y" }} | {{ post.categories | join: ', ' }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Ler mais...]({{ post.url }})

{% endfor %}

[Ver todas as publicações](/archive) | [Assinar via RSS](/feed.xml)

---

Última atualização: {{ site.time | date: "%d/%m/%Y" }}
