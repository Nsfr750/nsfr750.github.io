---
lang: de
lang-niv: fonto
lang-ref: 002-jbk
layout: page
title: 'Blog'
---

# Aktuelle Artikel

Willkommen in meinem Blog! Hier teile ich Tutorials, Projektaktualisierungen und Gedanken zu Technologie und Entwicklung.

## Neueste Beiträge

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Weiterlesen...]({{ post.url }})

{% endfor %}

[Alle Beiträge anzeigen](/archive) | [Nach Kategorien durchsuchen](/categories) | [Über RSS abonnieren](/feed.xml)

## Kategorien

- [3D-Druck](/category/3d-printing/)
- [Elektronik](/category/electronics/)
- [Python](/category/python/)
- [Anleitungen](/category/tutorials/)
- [Projektupdates](/category/updates/)

---

Zuletzt aktualisiert: {{ site.time | date: "%d.%m.%Y" }}
