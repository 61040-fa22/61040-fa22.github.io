---
title: Resources
layout: page
---

{%- for child in site.pages -%}
{%- if child.parent == page.title %}
- [{{ child.title }}]({%- link {{ child.path }} -%})
{%- endif -%}
{%- endfor -%}