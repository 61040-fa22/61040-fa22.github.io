---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Assignments
layout: assignments
---

Use [this form](https://forms.gle/CHheiJq4XhA88rjWA) to request slack days on assignments. Please consult the [class guide](https://61040-fa22.github.io/about/) first to make sure you know how our slack policies work.

{% for assignment in site.assignments %}
  <h2>
    <a href="{{ assignment.url }}">
      {{ assignment.title }}
    </a>
  </h2>
{% endfor %}