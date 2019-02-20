---
topics: jekyll
---

>{% assign categories = site.emptyArray %}
>{% for note in site.notes %}
>  {% assign categories = categories | concat:note.categories %}
>{% endfor %}