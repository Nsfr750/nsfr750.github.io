---
layout: category
category: %CATEGORY_NAME%
title: "%CATEGORY_TITLE%"
description: "%CATEGORY_DESCRIPTION%"
permalink: /category/%CATEGORY_NAME%/
---

# %CATEGORY_TITLE%

%CATEGORY_DESCRIPTION%

## Latest %CATEGORY_NAME% Articles

{% for post in site.categories.%CATEGORY_NAME% %}
### [{{ post.title }}]({{ post.url }})

{{ post.date | date: "%B %-d, %Y" }}

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Read more...]({{ post.url }})

{% endfor %}

[Back to Categories](categories/)
