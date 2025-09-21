---
title: Conference Proceedings
layout: default
permalink: /conference-proceedings
---

# Conference Proceedings

<ol class="pub-list">
{% for pub in site.data.publications_conference %}
  <li class="pub-item">
    <div class="pub-title"><em>{{ pub.title }}</em></div>
    <div class="pub-authors">{{ pub.authors }}</div>
    <div class="pub-meta">{{ pub.event }}{% if pub.year %}, {{ pub.year }}{% endif %}{% if pub.location %}, {{ pub.location }}{% endif %}{% if pub.note %}, {{ pub.note }}{% endif %}</div>
  </li>
{% endfor %}
</ol>
