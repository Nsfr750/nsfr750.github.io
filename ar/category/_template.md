---
layout: category
category: %CATEGORY_NAME%
title: "%CATEGORY_TITLE%"
description: "%CATEGORY_DESCRIPTION%"
permalink: /ar/category/%CATEGORY_NAME%/
lang: ar
dir: rtl
---

# %CATEGORY_TITLE%

%CATEGORY_DESCRIPTION%

## أحدث مقالات %CATEGORY_NAME%

{% for post in site.categories.%CATEGORY_NAME% %}
### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%d/%m/%Y" }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[اقرأ المزيد...]({{ post.url }})

{% endfor %}

[العودة إلى التصنيفات](/ar/categories/)
