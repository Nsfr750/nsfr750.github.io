---
lang: zh
lang-niv: fonto
lang-ref: 000-jbk
layout: index
title: '首页'
---

# 欢迎来到我的项目中心

你好！我是Nsfr750，一位充满激情的开发者和开源爱好者。在这里，我与世界分享我的项目、思考和发现。

## 最新博客文章

{% for post in site.posts limit:3 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[阅读更多...]({{ post.url }})

{% endfor %}

[查看所有文章](blog) | [按分类浏览](categories)

## 精选项目

以下是我最受欢迎的一些开源项目：

- [3D Filament Manager（3D线材管理器）](https://github.com/Nsfr750/3D_Filament_Manager) - 轻松管理您的3D打印线材
- [CDE550 Simulator（CDE550模拟器）](https://github.com/Nsfr750/CDE550-sim) - Nidec CDE550电机控制器模拟器
- [Email Duplicate Cleaner（邮件去重清理工具）](https://github.com/Nsfr750/EmailDuplicateCleaner) - 高效清理重复邮件

[查看所有项目](projects)

## 联系我

- [关于我](about) - 了解我的工作和兴趣
- [支持](support) - 喜欢我的作品？请考虑支持我
- [联系](contact) - 合作或提问

---

最后更新：{{ site.time | date: "%Y年%-m月%-d日" }}
