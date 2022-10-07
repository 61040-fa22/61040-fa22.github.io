---
title: Resources
layout: page
---

## Logistics
- [6.1040 general feedback form](http://tiny.cc/61040-fa22-feedback)
- [Slack day request form](https://docs.google.com/forms/d/e/1FAIpQLSc-bJbw168lnYE18Cn77yoEgprJIPZFbi2HnkJXzYHcb1epFg/viewform)

## Guides
<ul>
{%- for child in site.pages -%}
{%- if child.parent == page.title -%}
  <li><a href="{{ child.url }}">{{ child.title }}</a></li>
{%- endif -%}
{%- endfor -%}
</ul>

## External Links
- [Express.js official documentation](https://expressjs.com/)
- [express-session official documentation](https://www.npmjs.com/package/express-session)
- [Introduction to backend programming (MDN)](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Introduction)
- [Express tutorial (MDN)](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs)
