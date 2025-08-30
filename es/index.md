---
lang: es
lang-niv: fuente
lang-ref: 000-jbk
layout: index
title: 'Inicio'
---

# Bienvenido a Mi Centro de Proyectos

¡Hola! Soy Nsfr750, un desarrollador apasionado y entusiasta del código abierto. Aquí es donde comparto mis proyectos, pensamientos y descubrimientos con el mundo.

## Últimas Publicaciones del Blog

{% for post in site.posts limit:3 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Leer más...]({{ post.url }})

{% endfor %}

[Ver todas las publicaciones](blog) | [Explorar por categoría](categories)

## Proyectos Destacados

Aquí tienes algunos de mis proyectos de código abierto más populares:

- [3D Filament Manager](https://github.com/Nsfr750/3D_Filament_Manager) - Gestiona tus filamentos de impresión 3D con facilidad
- [Simulador CDE550](https://github.com/Nsfr750/CDE550-sim) - Simulador para el controlador de motor Nidec CDE550
- [Email Duplicate Cleaner](https://github.com/Nsfr750/EmailDuplicateCleaner) - Elimina correos electrónicos duplicados de manera eficiente

[Ver todos los proyectos](projects)

## Contáctame

- [Sobre Mí](about) - Conoce más sobre mi trabajo e intereses
- [Documentación](docs) - Guías detalladas de mis proyectos
- [Apoyo](support) - ¿Te gusta mi trabajo? Considera apoyarme
- [Contacto](contact) - Escríbeme para colaboraciones o preguntas

---

Última actualización: {{ site.time | date: "%d/%m/%Y" }}
