---
layout: page
title: Music
permalink: /works/music/
---
# Music

{% assign music_works = site.pages | where: "layout", "work" | where: "category", "music" | sort: "title" %}
{% if music_works.size > 0 %}
## Works
<ul class="work-list">
  {% for work in music_works %}
    <li><a href="{{ work.url | relative_url }}">{{ work.title }}</a></li>
  {% endfor %}
</ul>
{% else %}
No music works yet.
{% endif %}