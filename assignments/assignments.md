---
layout: page
title: "Assignments"
permalink: /assignments/
---


{% for post in site.posts reversed %}
{% if post.categories contains "assignments" %}
- [{{ post.title }}]({{post.url | relative_url}})
{% endif %}
{% endfor %}
