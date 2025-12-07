---
layout: default
title: Home
---
# Welcome to Jauhal.org

Here are my latest thoughts and writings:

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span style="color: #666; font-size: small;"> - {{ post.date | date_to_string }}</span>
    </li>
  {% endfor %}
</ul>
