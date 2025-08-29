---
lang: fr
lang-niv: fonto
lang-ref: 003-jbk
layout: page
title: 'Catégories'
---

# Catégories du Blog

Parcourez les articles par catégorie pour trouver le contenu qui vous intéresse le plus.

## Catégories Principales

- [Blog](/category/blog/) - Mises à jour et réflexions générales
- [Projets](/category/projects) - Vitrine de mon travail
- [Tutoriels](/category/tutorials) - Guides étape par étape
- [Technologie](/category/technology) - Aperçus et critiques technologiques
- [Développement](/category/development) - Programmation et sujets de codage

## Dernières Publications

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%d/%m/%Y" }} | {{ post.categories | join: ', ' }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Lire la suite...]({{ post.url }})

{% endfor %}

[Voir tous les articles](/archive) | [S'abonner via RSS](/feed.xml)

---

Dernière mise à jour : {{ site.time | date: "%d/%m/%Y" }}
