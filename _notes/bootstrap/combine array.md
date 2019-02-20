---
categories: bootstrap
---
<h1>Topics</h1>

{% assign categories = site.emptyArray %}
{% for note in site.notes %}
  {% assign categories = categories | concat:note.categories %}
{% endfor %}