---
lang: ru
lang-niv: fonto
lang-ref: 002-jbk
layout: page
title: 'Блог'
---

# Последние статьи

Добро пожаловать в мой блог! Здесь я делюсь обучающими материалами, обновлениями проектов и мыслями о технологиях и разработке.

## Последние записи

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Читать далее...]({{ post.url }})

{% endfor %}

[Все записи](/archive) | [Поиск по категориям](/categories) | [Подписаться через RSS](/feed.xml)

## Категории

- [3D-печать](/category/3d-printing/)
- [Электроника](/category/electronics/)
- [Python](/category/python/)
- [Руководства](/category/tutorials/)
- [Обновления проектов](/category/updates/)

---

Последнее обновление: {{ site.time | date: "%d.%m.%Y" }}
