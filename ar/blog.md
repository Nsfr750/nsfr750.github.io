---
lang: ar
dir: rtl
lang-niv: fonto
lang-ref: 002-jbk
layout: page
title: 'المدونة'
---

# أحدث المقالات

مرحباً بكم في مدونتي! هنا أشارك دروسًا وتحديثات المشاريع وأفكاري حول التكنولوجيا والتطوير.

## أحدث المنشورات

{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[اقرأ المزيد...]({{ post.url }})

{% endfor %}

[عرض جميع المقالات](archive) | [تصفح حسب التصنيف](categories) | [الاشتراك عبر RSS](feed.xml)

## التصنيفات

- [الطباعة ثلاثية الأبعاد](category/3d-printing/)
- [الإلكترونيات](category/electronics/)
- [تطوير البرمجيات](category/software-development/)
- [أدوات المطورين](category/developer-tools/)
- [مشاريع مفتوحة المصدر](category/open-source/)

## الأرشيف

تصفح المقالات القديمة في [صفحة الأرشيف](archive).

---

آخر تحديث: {{ site.time | date: "%d/%m/%Y" }}
