---
lang: en
lang-niv: fonto
lang-ref: 006-jbk
layout: page
title: 'Blog'
---


# Latest Articles

Welcome to my blog! Here I share tutorials, project updates, and thoughts on technology and development.

## Latest Posts

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Read more...]({{ post.url }})

{% endfor %}

[View all posts](/archive) | [Browse by category](/categories) | [Subscribe via RSS](/feed.xml)

## Categories

- [3D Printing](/category/3d-printing/)
- [Electronics](/category/electronics/)
- [Python](/category/python/)
- [Tutorials](/category/tutorials/)
- [Project Updates](/category/updates/)

---

Last updated: {{ site.time | date: "%B %-d, %Y" }}
