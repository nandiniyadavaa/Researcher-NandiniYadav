---
title: Poster Presentations
layout: default
permalink: /poster-presentations
---

# Poster Presentations

<ol class="pub-list">
{% for pub in site.data.publications_poster %}
  <li class="pub-item">
    <div class="pub-title"><em>{{ pub.title }}</em></div>
    <div class="pub-authors">{{ pub.authors }}</div>
    <div class="pub-meta">{{ pub.event }}{% if pub.year %}, {{ pub.year }}{% endif %}{% if pub.location %}, {{ pub.location }}{% endif %}{% if pub.note %}, {{ pub.note }}{% endif %}</div>
  </li>
{% endfor %}
</ol>
