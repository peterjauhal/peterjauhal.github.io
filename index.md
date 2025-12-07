---
layout: default
title: Home
---

# Welcome to peter jauhal's website

Here are my latest thoughts and writings:

{% for post in site.posts %}
- **[{{ post.title }}]({{ post.url }})** - *{{ post.date | date: "%B %d, %Y" }}*
{% endfor %}

Contact: public@jauhal.org
