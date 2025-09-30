---
title: Conference Proceedings
layout: default
permalink: /conference-proceedings
---

# Conference Proceedings

<ol class="pub-list">
{% for pub in site.data.publications_oral %}
  <li class="pub-item">
    <div class="pub-title"><em>{{ pub.title }}</em></div>
    <div class="pub-authors">{{ pub.authors }}</div>
    <div class="pub-meta">{{ pub.venue }}{% if pub.year %}, {{ pub.year }}{% endif %}{% if pub.location %}, {{ pub.location }}{% endif %},{% if pub.session %}, {{ pub.session }}{% endif %},{% if pub.link %}, {{ pub.link }}{% endif %},{% if pub.note %}, {{ pub.note }}{% endif %}</div>
  </li>
{% endfor %}
</ol>

