---
lang: it
lang-niv: fonto
lang-ref: 002-jbk
layout: page
title: 'Blog'
---

# Ultimi Articoli

Benvenuto nel mio blog! Qui condivido tutorial, aggiornamenti sui progetti e riflessioni su tecnologia e sviluppo.

## Ultimi Post

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Leggi tutto...]({{ post.url }})

{% endfor %}

[Vedi tutti i post](/archive) | [Sfoglia per categoria](/categories) | [Iscriviti via RSS](/feed.xml)

## Categorie

- [Stampa 3D](/category/3d-printing/)
- [Elettronica](/category/electronics/)
- [Python](/category/python/)
- [Tutorial](/category/tutorials/)
- [Aggiornamenti Progetti](/category/updates/)

---

Ultimo aggiornamento: {{ site.time | date: "%d/%m/%Y" }}
