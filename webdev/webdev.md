---
layout: page
title: "WebDev"
permalink: /webdev-materials/
---

{% for post in site.posts reversed %}
{% if post.categories contains "webdev" %}
- [{{ post.title }}]({{post.url | relative_url}})
{% endif %}
{% endfor %}
