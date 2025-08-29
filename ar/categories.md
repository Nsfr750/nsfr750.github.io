---
lang: ar
dir: rtl
lang-niv: fonto
lang-ref: 003-jbk
layout: page
title: 'التصنيفات'
---

# تصنيفات المدونة

تصفح المقالات حسب التصنيف للعثور على المحتوى الذي يهمك أكثر.

## التصنيفات الرئيسية

- [المدونة](/category/blog/) - تحديثات عامة وأفكار
- [المشاريع](/category/projects) - عرض لأعمالي
- [الدروس](/category/tutorials) - خطوات إرشادية خطوة بخطوة
- [التكنولوجيا](/category/technology) - رؤى وتقييمات تقنية
- [التطوير](/category/development) - مواضيع البرمجة والترميز

## أحدث المقالات

{% for post in site.posts limit:5 %}

### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%d/%m/%Y" }} | {{ post.categories | join: '، ' }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[اقرأ المزيد...]({{ post.url }})

{% endfor %}

[عرض جميع المقالات](/archive) | [عرض جميع التصنيفات](/categories)

---

آخر تحديث: {{ site.time | date: "%d/%m/%Y" }}
