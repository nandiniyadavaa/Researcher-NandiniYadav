---
title: Publications
layout: default
permalink: /publications
---

# Publications

## Recently Submitted
{% for pub in site.data.publications_recent %}
[{{ pub.title }}]({{ pub.link }})  
{{ pub.authors }}  
{%- if pub.journal -%}*{{ pub.journal }}*{%- endif -%}{% if pub.year %}{% if pub.journal %}, {% endif %}{{ pub.year }}{% endif %}

{% endfor %}

## Peer-Reviewed Articles
{% for pub in site.data.publications_peerreviewed %}
[{{ pub.title }}]({{ pub.link }})  
{{ pub.authors }}  
{%- if pub.journal -%}*{{ pub.journal }}*{%- endif -%}{% if pub.year %}{% if pub.journal %}, {% endif %}{{ pub.year }}{% endif %}

{% endfor %}

## Conference Proceedings
<ol class="pub-list">
{% for pub in site.data.publications_conference %}
  <li class="pub-item">
    <div class="pub-title"><em>{{ pub.title }}</em></div>
    <div class="pub-authors">{{ pub.authors }}</div>
    {%- assign parts = "" -%}
    {%- if pub.venue -%}{%- assign parts = parts | append: "<strong>" | append: pub.venue | append: "</strong>" -%}{%- endif -%}
    {%- if pub.location -%}{%- if parts != "" -%}{%- assign parts = parts | append: ", " -%}{%- endif -%}{%- assign parts = parts | append: pub.location -%}{%- endif -%}
    {%- if pub.year -%}{%- if parts != "" -%}{%- assign parts = parts | append: ", " -%}{%- endif -%}{%- assign parts = parts | append: pub.year -%}{%- endif -%}
    {%- if pub.session -%}{%- if parts != "" -%}{%- assign parts = parts | append: " — " -%}{%- endif -%}{%- assign parts = parts | append: "Session " | append: pub.session -%}{%- endif -%}
    {%- if pub.link -%}{%- if parts != "" -%}{%- assign parts = parts | append: " • " -%}{%- endif -%}{%- assign parts = parts | append: '<a href="' | append: pub.link | append: '" target="_blank" rel="noopener">link</a>' -%}{%- endif -%}
    {%- if pub.note -%}{%- if parts != "" -%}{%- assign parts = parts | append: " • " -%}{%- endif -%}{%- assign parts = parts | append: pub.note -%}{%- endif -%}
    <div class="pub-meta">{{ parts }}</div>
  </li>
{% endfor %}
</ol>

## Oral Presentations
{% for pub in site.data.publications_oral %}
**{{ pub.title }}**  
{{ pub.authors }}  
{%- if pub.venue -%}*{{ pub.venue }}*{%- endif -%}{% if pub.location %}, {{ pub.location }}{% endif %}{% if pub.year %}, {{ pub.year }}{% endif %}{% if pub.session %}, Session {{ pub.session }}{% endif %}{% if pub.link %}, <a href="{{ pub.link }}" target="_blank" rel="noopener">link</a>{% endif %}

{% endfor %}

## Poster Presentations
{% for pub in site.data.publications_poster %}
**{{ pub.title }}**  
{{ pub.authors }}  
{%- if pub.venue -%}*{{ pub.venue }}*{%- endif -%}{% if pub.location %}, {{ pub.location }}{% endif %}{% if pub.year %}, {{ pub.year }}{% endif %}{% if pub.session %}, Session {{ pub.session }}{% endif %}{% if pub.link %}, <a href="{{ pub.link }}" target="_blank" rel="noopener">link</a>{% endif %}

{% endfor %}
