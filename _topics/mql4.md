---
name: mql4
full_name: mql4
tags: [mql4,mt4]
---
mql4 language related stuff

{% assign page_tags_c = page.tags | size %}
{% for p in page.tags  %}
  {{p}}<br />
{% endfor %}
{{page_tags_c}}
<hr />
<ul>
  {% for note in site.notes %}
  
    {% assign note_tags_c = note.tags | size | plus: page_tags_c  %}

    {% assign combine_tags = page.tags | combine: note.tags %}
    {% assign combine_tags_u = combine_tags | uniq %}
    {% assign combine_tags_c = combine_tags_u | size %}
    
    {% for p in combine_tags_u  %}
      {{p}}<br />
    {% endfor %}
    {% if note_tags_c > combine_tags_c %}
      -----
    {% endif %}
    <hr />
  {% endfor %}
  
</ul>