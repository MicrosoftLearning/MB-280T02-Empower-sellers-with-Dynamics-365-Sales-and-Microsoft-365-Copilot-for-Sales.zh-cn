---
title: 练习说明
permalink: index.html
layout: home
---

# 练习

此页列出了与 [Microsoft Learn](https://learn.microsoft.com) 上的 Microsoft 技能内容关联的练习

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %} {% for activity in labs  %}
- [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) {% endfor %}

