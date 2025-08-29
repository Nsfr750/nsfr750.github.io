---
lang: es
lang-niv: fonto
lang-ref: 003-jbk
layout: page
title: 'Categorías'
---

# Categorías del Blog

Explora los artículos por categoría para encontrar el contenido que más te interese.

## Categorías Principales

- [Blog](/category/blog/) - Actualizaciones y reflexiones generales
- [Proyectos](/category/projects) - Muestra de mi trabajo
- [Tutoriales](/category/tutorials) - Guías paso a paso
- [Tecnología](/category/technology) - Análisis y reseñas tecnológicas
- [Desarrollo](/category/development) - Programación y temas de codificación

## Últimas Publicaciones

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%d/%m/%Y" }} | {{ post.categories | join: ', ' }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Leer más...]({{ post.url }})

{% endfor %}

[Ver todas las publicaciones](/archive) | [Suscríbete vía RSS](/feed.xml)

---

Última actualización: {{ site.time | date: "%d/%m/%Y" }}
