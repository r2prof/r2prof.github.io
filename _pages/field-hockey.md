---
title: "Field Hockey"
permalink: /field-hockey/
layout: archive
author_profile: true
---

Everything field hockey — games, notes, whatever's relevant. More to come here.

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'field-hockey'" %}
{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}
