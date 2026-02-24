---
layout: page
title: Art
permalink: /works/art/
---
# Art

{% assign art_works = site.pages | where: "layout", "work" | where: "category", "art" | sort: "title" %}
{% if art_works.size > 0 %}
## Works
<ul class="work-list">
  {% for work in art_works %}
    <li><a href="{{ work.url | relative_url }}">{{ work.title }}</a></li>
  {% endfor %}
</ul>
{% else %}
No art works yet.
{% endif %}