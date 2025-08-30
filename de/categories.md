---
lang: de
lang-niv: fonto
lang-ref: 003-jbk
layout: page
title: 'Kategorien'
---

# Blog-Kategorien

Durchsuchen Sie Artikel nach Kategorien, um Inhalte zu finden, die Sie am meisten interessieren.

## Hauptkategorien

- [Blog](category/blog/) - Allgemeine Updates und Gedanken
- [Projekte](category/projects) - Vorstellung meiner Arbeiten
- [Anleitungen](category/tutorials) - Schritt-für-Schritt-Anleitungen
- [Technologie](category/technology) - Technische Einblicke und Bewertungen
- [Entwicklung](category/development) - Programmierung und Codierungsthemen

## Neueste Beiträge

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%d.%m.%Y" }} | {{ post.categories | join: ', ' }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Weiterlesen...]({{ post.url }})

{% endfor %}

[Alle Beiträge anzeigen](archive) | [Über RSS abonnieren](feed.xml)

---

Zuletzt aktualisiert: {{ site.time | date: "%d.%m.%Y" }}
