---
name: mql4
full_name: mql4
tags: [mql4,mt4]
---
mql4 language related stuff

{% assign page_tags_c = page.tags | size %}
<ul>
  {% for note in site.notes %}
    {% assign total_tags_c = note.tags | size %}
    {% assign total_tags_c = total_tags_c + page_tags_c %}
{{total_tags_c}}
    {% assign combine_tags_c = page.tags | combine: note.tags | uniq %}
    
  {% endfor %}
  
</ul>