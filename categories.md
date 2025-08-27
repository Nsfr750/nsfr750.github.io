---
layout: page
title: Categories
description: Browse articles by category - Nsfr750's blog about technology, programming, and projects
permalink: /categories/
---

# Blog Categories

Browse articles by category to find content that interests you most.

## Main Categories

- [Blog](/category/blog/) - General updates and thoughts
- [Projects](/category/projects/) - Showcase of my work
- [Tutorials](/category/tutorials/) - Step-by-step guides
- [Technology](/category/technology/) - Tech insights and reviews
- [Development](/category/development/) - Programming and coding topics

## Latest Posts

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%B %-d, %Y" }} | {{ post.categories | join: ', ' }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Read more...]({{ post.url }})

{% endfor %}

[View all posts](/archive) | [Subscribe via RSS](/feed.xml)

---

Last updated: {{ site.time | date: "%B %-d, %Y" }}
