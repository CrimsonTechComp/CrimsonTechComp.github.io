---
layout: page
title: "Intro"
permalink: /intro-materials/
---

The following are the intro labs.
{% for post in site.posts %}
{% if post.categories contains "intro" %}
- [{{ post.title }}]({{post.url | relative_url}})
{% endif %}
{% endfor %}
