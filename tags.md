---
layout: page
title: 标签
permalink: tags
---
<div class="tags">
{% for collections in site.collections %}
  {% if collections.label == "my_tags" %}
    {% for doc in collections.docs %}
        <a href="{{ site.baseurl }}tag/{{ doc.slug }}">{{ doc.name }}</a>
    {% endfor %}
  {% endif %}
{% endfor %}
</div>
