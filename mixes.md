---
title: ":mixes"
layout: page
permalink: /mixes
---

# My latest mixes

<ul>
  {% for category in site.categories %}
    {% if category[0] == 'mix' %}
      <ul>
      {% for post in category[1] %}
        <li>
          <a href="{{ post.url | relative_url }}">[{{ post.date | date: '%Y-%m-%d' }}] {{ post.title }}</a>
        </li>
      {% endfor %}
      </ul>
    {% endif %}
  {% endfor %}
</ul>
