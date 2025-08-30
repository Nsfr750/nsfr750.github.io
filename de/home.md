---
lang: de
lang-niv: quelle
lang-ref: 001-jbk
layout: page
title: 'Startseite'
---

# Willkommen in meinem Projekt-Hub

Hallo! Ich bin Nsfr750, ein leidenschaftlicher Entwickler und Open-Source-Enthusiast. Hier teile ich meine Projekte, Gedanken und Entdeckungen mit der Welt.

## Neueste Blog-Beiträge

{% for post in site.posts limit:3 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Weiterlesen...]({{ post.url }})

{% endfor %}

[Alle Beiträge anzeigen](blog) | [Nach Kategorie durchsuchen](categories)

## Ausgewählte Projekte

Hier sind einige meiner beliebtesten Open-Source-Projekte:

- [3D Filament Manager](https://github.com/Nsfr750/3D_Filament_Manager) - Verwalten Sie Ihre 3D-Druckfilamente mit Leichtigkeit
- [CDE550 Simulator](https://github.com/Nsfr750/CDE550-sim) - Simulator für den Nidec CDE550 Motorcontroller
- [Email Duplicate Cleaner](https://github.com/Nsfr750/EmailDuplicateCleaner) - Bereinigen Sie doppelte E-Mails effizient
