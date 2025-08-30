---
lang: zh
lang-niv: fonto
lang-ref: 003-jbk
layout: page
title: '分类'
---

# 博客分类

按分类浏览文章，找到最吸引您的内容。

## 主要分类

- [博客](category/blog/) - 一般更新和思考
- [项目](category/projects) - 展示我的作品
- [教程](category/tutorials) - 分步指南
- [技术](category/technology) - 技术洞察和评测
- [开发](category/development) - 编程和编码主题

## 最新文章

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%Y年%-m月%-d日" }} | {{ post.categories | join: '、' }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[阅读更多...]({{ post.url }})

{% endfor %}

[查看所有文章](archive) | [通过RSS订阅](feed.xml)

---

最后更新：{{ site.time | date: "%Y年%-m月%-d日" }}
