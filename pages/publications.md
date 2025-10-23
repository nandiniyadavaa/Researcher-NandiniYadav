---
title: Publications
layout: default
permalink: /publications
---

# Publications



## Peer-Reviewed Articles
<ol class="pub-list">
{% for pub in site.data.publications_peerreviewed %}
  <li class="pub-item">
    <div class="pub-title">
      {% if pub.link %}
        <a href="{{ pub.link }}" target="_blank" rel="noopener"><em>{{ pub.title }}</em></a>
      {% elsif pub.doi %}
        <a href="https://doi.org/{{ pub.doi | strip }}" target="_blank" rel="noopener"><em>{{ pub.title }}</em></a>
      {% else %}
        <em>{{ pub.title }}</em>
      {% endif %}
    </div>

    <div class="pub-authors">{{ pub.authors }}</div>

    {%- assign parts = "" -%}
    {%- if pub.journal -%}{%- assign parts = parts | append: "<em>" | append: pub.journal | append: "</em>" -%}{%- endif -%}
    {%- if pub.year -%}{%- if parts != "" -%}{%- assign parts = parts | append: ", " -%}{%- endif -%}{%- assign parts = parts | append: pub.year -%}{%- endif -%}
    {%- if pub.volume -%}{%- if parts != "" -%}{%- assign parts = parts | append: ", " -%}{%- endif -%}{%- assign parts = parts | append: pub.volume -%}{%- if pub.issue -%}{%- assign parts = parts | append: " (" | append: pub.issue | append: ")" -%}{%- endif -%}{%- endif -%}
    {%- if pub.pages -%}{%- if parts != "" -%}{%- assign parts = parts | append: ", " -%}{%- endif -%}{%- assign parts = parts | append: pub.pages -%}{%- endif -%}
    {%- if pub.doi -%}{%- if parts != "" -%}{%- assign parts = parts | append: " • " -%}{%- endif -%}{%- assign parts = parts | append: '<a href="https://doi.org/' | append: pub.doi | append: '" target="_blank" rel="noopener">doi:' | append: pub.doi | append: '</a>' -%}{%- endif -%}
    {%- if pub.link and (pub.doi == nil or pub.doi == '') -%}{%- if parts != "" -%}{%- assign parts = parts | append: " • " -%}{%- endif -%}{%- assign parts = parts | append: '<a href="' | append: pub.link | append: '" target="_blank" rel="noopener">link</a>' -%}{%- endif -%}
    {%- if pub.note -%}{%- if parts != "" -%}{%- assign parts = parts | append: " • " -%}{%- endif -%}{%- assign parts = parts | append: pub.note -%}{%- endif -%}

    <div class="pub-meta">{{ parts }}</div>
  </li>
{% endfor %}
</ol>

## Conference proceedings
<ol class="pub-list">
{% for pub in site.data.publications_peerreviewed %}
  <li class="pub-item">
    <div class="pub-title">
      {% if pub.link %}
        <a href="{{ pub.link }}" target="_blank" rel="noopener"><em>{{ pub.title }}</em></a>
      {% elsif pub.doi %}
        <a href="https://doi.org/{{ pub.doi | strip }}" target="_blank" rel="noopener"><em>{{ pub.title }}</em></a>
      {% else %}
        <em>{{ pub.title }}</em>
      {% endif %}
    </div>

    <div class="pub-authors">{{ pub.authors }}</div>

    {%- assign parts = "" -%}
    {%- if pub.journal -%}{%- assign parts = parts | append: "<em>" | append: pub.journal | append: "</em>" -%}{%- endif -%}
    {%- if pub.year -%}{%- if parts != "" -%}{%- assign parts = parts | append: ", " -%}{%- endif -%}{%- assign parts = parts | append: pub.year -%}{%- endif -%}
    {%- if pub.volume -%}{%- if parts != "" -%}{%- assign parts = parts | append: ", " -%}{%- endif -%}{%- assign parts = parts | append: pub.volume -%}{%- if pub.issue -%}{%- assign parts = parts | append: " (" | append: pub.issue | append: ")" -%}{%- endif -%}{%- endif -%}
    {%- if pub.pages -%}{%- if parts != "" -%}{%- assign parts = parts | append: ", " -%}{%- endif -%}{%- assign parts = parts | append: pub.pages -%}{%- endif -%}
    {%- if pub.doi -%}{%- if parts != "" -%}{%- assign parts = parts | append: " • " -%}{%- endif -%}{%- assign parts = parts | append: '<a href="https://doi.org/' | append: pub.doi | append: '" target="_blank" rel="noopener">doi:' | append: pub.doi | append: '</a>' -%}{%- endif -%}
    {%- if pub.link and (pub.doi == nil or pub.doi == '') -%}{%- if parts != "" -%}{%- assign parts = parts | append: " • " -%}{%- endif -%}{%- assign parts = parts | append: '<a href="' | append: pub.link | append: '" target="_blank" rel="noopener">link</a>' -%}{%- endif -%}
    {%- if pub.note -%}{%- if parts != "" -%}{%- assign parts = parts | append: " • " -%}{%- endif -%}{%- assign parts = parts | append: pub.note -%}{%- endif -%}

    <div class="pub-meta">{{ parts }}</div>
  </li>
{% endfor %}
</ol>


