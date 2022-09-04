---
title: Resources
layout: page
---

<ul>
{%- for child in site.pages -%}
{%- if child.parent == page.title -%}
  <li><a href="{{ child.url }}">{{ child.title }}</a></li>
{%- endif -%}
{%- endfor -%}
</ul>