---
layout: default
title: Home
---

# 🧭 darrell.thoughts

Welcome to my public journal of ideas, logs, and explorations.

---

{% assign categories = site.posts | map: "category" | uniq | sort %}

{% for cat in categories %}
## 🗂️ {{ cat | capitalize }}

<ul>
  {% for post in site.posts %}
    {% if post.category == cat %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a> – <small>{{ post.date | date: "%b %d, %Y" }}</small>
      </li>
    {% endif %}
  {% endfor %}
</ul>
{% endfor %}
