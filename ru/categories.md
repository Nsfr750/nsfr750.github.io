---
lang: ru
lang-niv: fonto
lang-ref: 003-jbk
layout: page
title: 'Категории'
---

# Категории блога

Просматривайте статьи по категориям, чтобы найти наиболее интересный для вас контент.

## Основные категории

- [Блог](category/blog/) - Общие обновления и мысли
- [Проекты](category/projects) - Примеры моих работ
- [Руководства](category/tutorials) - Пошаговые инструкции
- [Технологии](category/technology) - Технические обзоры и анализ
- [Разработка](category/development) - Программирование и кодинг

## Последние записи

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%d.%m.%Y" }} | {{ post.categories | join: ', ' }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Читать далее...]({{ post.url }})

{% endfor %}

[Все записи](archive) | [Подписаться через RSS](feed.xml)

---

Последнее обновление: {{ site.time | date: "%d.%m.%Y" }}
