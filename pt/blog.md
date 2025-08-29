---
lang: pt
lang-niv: fonto
lang-ref: 002-jbk
layout: page
title: 'Blog'
---

# Artigos Recentes

Bem-vindo ao meu blog! Aqui compartilho tutoriais, atualizações de projetos e reflexões sobre tecnologia e desenvolvimento.

## Publicações Recentes

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Ler mais...]({{ post.url }})

{% endfor %}

[Ver todas as publicações](/archive) | [Navegar por categoria](/categories) | [Assinar via RSS](/feed.xml)

## Categorias

- [Impressão 3D](/category/3d-printing/)
- [Eletrônica](/category/electronics/)
- [Python](/category/python/)
- [Tutoriais](/category/tutorials/)
- [Atualizações de Projetos](/category/updates/)

---

Última atualização: {{ site.time | date: "%d/%m/%Y" }}
