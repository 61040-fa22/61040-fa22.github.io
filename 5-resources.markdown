---
title: Resources
layout: page
---

- [6.1040 general feedback form](http://tiny.cc/61040-fa22-feedback)

{%- for child in site.pages -%}
{%- if child.parent == page.title -%}
- [{{ child.title }}]({{ child.url }})
{%- endif -%}
{%- endfor -%}

- [Express.js official documentation](https://expressjs.com/)
- [express-session](https://www.npmjs.com/package/express-session)
- [Introduction to backend programming (MDN)](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Introduction)
- [Express tutorial (MDN)](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs)
- [Cookies (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
