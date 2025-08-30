---
lang: pt
lang-niv: fonte
lang-ref: 001-jbk
layout: page
title: 'Início'
---

# Bem-vindo ao Meu Hub de Projetos

Olá! Eu sou o Nsfr750, um desenvolvedor apaixonado e entusiasta de código aberto. É aqui que compartilho meus projetos, pensamentos e descobertas com o mundo.

## Últimas Postagens do Blog

{% for post in site.posts limit:3 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Leia mais...]({{ post.url }})

{% endfor %}

[Ver todas as postagens](blog) | [Navegar por categoria](categories)

## Projetos em Destaque

Aqui estão alguns dos meus projetos de código aberto mais populares:

- [3D Filament Manager](https://github.com/Nsfr750/3D_Filament_Manager) - Gerencie seus filamentos de impressão 3D com facilidade
- [Simulador CDE550](https://github.com/Nsfr750/CDE550-sim) - Simulador para o controlador de motor Nidec CDE550
- [Email Duplicate Cleaner](https://github.com/Nsfr750/EmailDuplicateCleaner) - Limpe e-mails duplicados de forma eficiente
