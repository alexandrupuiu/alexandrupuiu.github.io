---
layout: single
classes: wide
permalink: /PerTopic/
title: "Per Topic"
author_profile: true
header:
  image: 
  image_description: "Near Aachen, Germany"
  caption: "Photo credit: [**Ohcapi**](https://ohcapi.com)"
---



{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}---
