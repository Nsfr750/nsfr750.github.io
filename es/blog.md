---
lang: es
lang-niv: fonto
lang-ref: 002-jbk
layout: page
title: 'Blog'
---

# Últimos Artículos

¡Bienvenido a mi blog! Aquí comparto tutoriales, actualizaciones de proyectos y reflexiones sobre tecnología y desarrollo.

## Últimas Publicaciones

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Leer más...]({{ post.url }})

{% endfor %}

[Ver todas las publicaciones](archive) | [Explorar por categoría](categories) | [Suscríbete vía RSS](feed.xml)

## Categorías

- [Impresión 3D](category/3d-printing/)
- [Electrónica](category/electronics/)
- [Python](category/python/)
- [Tutoriales](category/tutorials/)
- [Actualizaciones de Proyectos](category/updates/)

---

Última actualización: {{ site.time | date: "%d/%m/%Y" }}
