---
lang: en
lang-niv: fonto
lang-ref: 000-jbk
layout: index
title: 'Home'
---

# Welcome to My Project Hub

Hi there! I'm Nsfr750, a passionate developer and open-source enthusiast. This is where I share my projects, thoughts, and discoveries with the world.

## Latest Blog Posts

{% for post in site.posts limit:3 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Read more...]({{ post.url }})

{% endfor %}

[View all posts](blog) | [Browse by category](categories)

## Featured Projects

Here are some of my most popular open-source projects:

- [3D Filament Manager](https://github.com/Nsfr750/3D_Filament_Manager) - Manage your 3D printing filaments with ease
- [CDE550 Simulator](https://github.com/Nsfr750/CDE550-sim) - Simulator for Nidec CDE550 motor controller
- [Email Duplicate Cleaner](https://github.com/Nsfr750/EmailDuplicateCleaner) - Clean up duplicate emails efficiently
