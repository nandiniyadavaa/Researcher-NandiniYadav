---
title: Recently Submitted
layout: default
permalink: /recently-submitted
---

# Recently Submitted

<ol class="pub-list">
{% for pub in site.data.publications_recent %}
  <li class="pub-item">
    <div class="pub-title"><em>{{ pub.title }}</em></div>
    <div class="pub-authors">{{ pub.authors }}</div>
    <div class="pub-meta">{{ pub.journal }}{% if pub.year %}, {{ pub.year }}{% endif %}{% if pub.note %}, {{ pub.note }}{% endif %}</div>
  </li>
{% endfor %}
</ol>
