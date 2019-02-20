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
    {{note_tags_c}}<br />
    {{page_tags_c}}<br />
    {% assign total_tags_c = note_tags_c | plus: page_tags_c %}
    {{total_tags_c}}<br />
    {% assign combine_tags_c = page.tags | combine: note.tags | uniq %}

    
    {% for p in note.tags  %}
      {{p}}<br />
    {% endfor %}
    {% if total_tags_c > combine_tags_c%}
      -----
    {% endif %}
    <hr />
  {% endfor %}
  
</ul>