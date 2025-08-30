---
lang: ru
lang-niv: fonto
lang-ref: 000-jbk
layout: index
title: 'Главная'
---

# Добро пожаловать в мой проект-хаб

Привет! Я Nsfr750, увлеченный разработчик и энтузиаст открытого ПО. Здесь я делюсь своими проектами, мыслями и открытиями со всем миром.

## Последние записи в блоге

{% for post in site.posts limit:3 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Читать далее...]({{ post.url }})

{% endfor %}

[Все записи](blog) | [Поиск по категориям](categories)

## Избранные проекты

Вот некоторые из моих самых популярных проектов с открытым исходным кодом:

- [3D Filament Manager](https://github.com/Nsfr750/3D_Filament_Manager) - Удобное управление нитями для 3D-печати
- [CDE550 Simulator](https://github.com/Nsfr750/CDE550-sim) - Симулятор контроллера двигателя Nidec CDE550
- [Email Duplicate Cleaner](https://github.com/Nsfr750/EmailDuplicateCleaner) - Эффективная очистка дубликатов электронных писем

[Все проекты](projects)

## Свяжитесь со мной

- [Обо мне](about) - Узнайте больше о моей работе и интересах
- [Поддержка](support) - Нравится моя работа? Рассмотрите возможность поддержки
- [Контакты](contact) - Свяжитесь для сотрудничества или вопросов

---

Последнее обновление: {{ site.time | date: "%d.%m.%Y" }}
