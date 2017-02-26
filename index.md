---
layout: default
title: Home sweet home
---
## {{ page.title }}

All posts
{% for post in site.posts %}
  - {{ post.date | date_to_string}} [{{ post.title }}]({{ post.url }})
{% endfor %}

All pages
{% for page in site.pages %}
  - [{{ page.title }}]({{ page.url }})
{% endfor %}
