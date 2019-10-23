---
title: "blogposts"
layout: page
permalink: /blogposts
---

# My latest blogposts

Work in progress!

<ul>
  {% for category in site.categories %}
    {% if category[0] == 'blogpost' %}
      <ul>
      {% for post in category[1] %}
        <li>
          <a href="{{ post.url | relative_url }}">[{{ post.date | date: '%Y-%m-%d'}}] {{ post.title }}</a>
        </li>
      {% endfor %}
      </ul>
    {% endif %}
  {% endfor %}
</ul>
