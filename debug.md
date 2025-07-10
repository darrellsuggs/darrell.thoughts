---
layout: default
title: Debug Site Categories
permalink: /debug/
---

# Debug: site.categories

{% for category in site.categories %}
## Category: **{{ category[0] }}**
- Found **{{ category[1] | size }}** posts
<ul>
  {% for post in category[1] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
{% endfor %}

