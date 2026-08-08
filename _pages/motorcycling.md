---
title: "Motorcycling"
permalink: /motorcycling/
layout: archive
author_profile: true
---

Notes on learning to ride, gear, and the occasional trip. I completed the NJ Motorcycle Rider Training course and am building out a gear kit with a strong bias toward safety certification over brand — if you're new to this too, that's roughly the filter I use for anything I post here.

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'motorcycling'" %}
{% for post in posts %}
  {% include archive-single.html %}
{% endfor %}
