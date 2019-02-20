---
name: mql4
full_name: mql4
tags: [mql4,mt4]
---
an object-oriented programming language, was written specifically for work on MT4. Syntax based on C.



<ul>
  {% for note in site.notes %}
    {% if note.tags contains page.tags %}
        <li>
        <h2><a href="{{ topic.url }}">{{ topic.name }}</a></h2>
        <p>{{ topic.content | markdownify }}</p>
        </li>
    {% endif %}
  {% endfor %}
  
</ul>