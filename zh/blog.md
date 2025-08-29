---
lang: zh
lang-niv: fonto
lang-ref: 002-jbk
layout: page
title: '博客'
---

# 最新文章

欢迎来到我的博客！在这里，我分享教程、项目更新以及技术和开发相关的思考。

## 最新文章

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[阅读更多...]({{ post.url }})

{% endfor %}

[查看所有文章](/archive) | [按分类浏览](/categories) | [通过RSS订阅](/feed.xml)

## 分类

- [3D打印](/category/3d-printing/)
- [电子技术](/category/electronics/)
- [Python](/category/python/)
- [教程](/category/tutorials/)
- [项目更新](/category/updates/)

---

最后更新：{{ site.time | date: "%Y年%-m月%-d日" }}
