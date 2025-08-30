---
lang: fr
lang-niv: fonto
lang-ref: 002-jbk
layout: page
title: 'Blog'
---

# Derniers Articles

Bienvenue sur mon blog ! Ici, je partage des tutoriels, des mises à jour de projets et des réflexions sur la technologie et le développement.

## Dernières Publications

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Lire la suite...]({{ post.url }})

{% endfor %}

[Voir tous les articles](archive) | [Parcourir par catégorie](categories) | [S'abonner via RSS](feed.xml)

## Catégories

- [Impression 3D](category/3d-printing/)
- [Électronique](category/electronics/)
- [Python](category/python/)
- [Tutoriels](category/tutorials/)
- [Mises à jour de Projets](category/updates/)

---

Dernière mise à jour : {{ site.time | date: "%d/%m/%Y" }}
