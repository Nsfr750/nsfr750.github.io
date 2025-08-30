---
lang: it
lang-niv: fonto
lang-ref: 003-jbk
layout: page
title: 'Categorie'
---

# Categorie del Blog

Sfoglia gli articoli per categoria per trovare i contenuti che ti interessano di più.

## Categorie Principali

- [Blog](category/blog/) - Aggiornamenti e pensieri generali
- [Progetti](category/projects) - Vetrina dei miei lavori
- [Tutorial](category/tutorials) - Guide passo dopo passo
- [Tecnologia](category/technology) - Approfondimenti e recensioni tecnologiche
- [Sviluppo](category/development) - Programmazione e argomenti di codifica

## Ultimi Post

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%d/%m/%Y" }} | {{ post.categories | join: ', ' }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Leggi tutto...]({{ post.url }})

{% endfor %}

[Vedi tutti i post](archive) | [Iscriviti via RSS](feed.xml)

---

Ultimo aggiornamento: {{ site.time | date: "%d/%m/%Y" }}
