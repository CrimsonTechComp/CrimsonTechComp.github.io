---
layout: page
title: "Python"
permalink: /python-materials/
---

{% for post in site.posts reversed %}
{% if post.categories contains "python" %}
- [{{ post.title }}]({{post.url | relative_url}})
{% endif %}
{% endfor %}
