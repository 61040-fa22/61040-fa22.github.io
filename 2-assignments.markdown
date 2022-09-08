---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Assignments
layout: assignments
---

{% for assignment in site.assignments %}
  <h2>
    <a href="{{ assignment.url }}">
      {{ assignment.title }}
    </a>
  </h2>
{% endfor %}