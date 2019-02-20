---
name: mql4
full_name: MetaQuotes Language 4
tags: [mql4,mt4]
---
>MetaQuotes Language 4 (MQL4) is a built-in language for programming trading strategies. This language is developed by MetaQuotes Software Corp. based on their long experience in the creation of online trading platforms. Using this language, you can create your own Expert Advisors that make trading management automated and are perfectly suitable for implementing your own trading strategies. Besides, using MQL4 you can create your own technical indicators (custom indicators), scripts and libraries.

{% assign page_tags_c = page.tags | size %}

{% for note in site.notes %}

  {% assign note_tags_c = note.tags | size | plus: page_tags_c  %}

  {% assign combine_tags = page.tags | combine: note.tags %}
  {% assign combine_tags_u = combine_tags | uniq %}
  {% assign combine_tags_c = combine_tags_u | size %}
  
  {% if note_tags_c > combine_tags_c %}
    [note.title](note.url)
  {% endif %}
{% endfor %}
