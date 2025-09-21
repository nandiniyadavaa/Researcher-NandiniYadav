---
title: Peer-reviewed Publications
layout: default
permalink: /peer-reviewed-publications
---

# Peer-reviewed Publications

<ol class="pub-list">
{% for pub in site.data.publications_peerreviewed %}
  <li class="pub-item">
    <div class="pub-title"><em>{{ pub.title }}</em></div>
    <div class="pub-authors">{{ pub.authors }}</div>
    <div class="pub-meta">{{ pub.journal }}{% if pub.year %}, {{ pub.year }}{% endif %}{% if pub.pages %}, {{ pub.pages }}{% endif %}</div>
  </li>
{% endfor %}
</ol>
