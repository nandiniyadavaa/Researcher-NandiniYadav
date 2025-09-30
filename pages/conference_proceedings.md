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

    {%- assign parts = "" -%}
    {%- if pub.venue -%}
      {%- assign parts = parts | append: "<strong>" | append: pub.venue | append: "</strong>" -%}
    {%- endif -%}

    {%- if pub.location -%}
      {%- if parts != "" -%}{%- assign parts = parts | append: ", " -%}{%- endif -%}
      {%- assign parts = parts | append: pub.location -%}
    {%- endif -%}

    {%- if pub.year -%}
      {%- if parts != "" -%}{%- assign parts = parts | append: ", " -%}{%- endif -%}
      {%- assign parts = parts | append: pub.year -%}
    {%- endif -%}

    {%- if pub.session -%}
      {%- if parts != "" -%}{%- assign parts = parts | append: " — " -%}{%- endif -%}
      {%- assign parts = parts | append: "Session " | append: pub.session -%}
    {%- endif -%}

    {%- if pub.link -%}
      {%- if parts != "" -%}{%- assign parts = parts | append: " • " -%}{%- endif -%}
      {%- assign parts = parts | append: '<a href="' | append: pub.link | append: '" target="_blank" rel="noopener">link</a>' -%}
    {%- endif -%}

    {%- if pub.note -%}
      {%- if parts != "" -%}{%- assign parts = parts | append: " • " -%}{%- endif -%}
      {%- assign parts = parts | append: pub.note -%}
    {%- endif -%}

    <div class="pub-meta">{{ parts }}</div>
  </li>
{% endfor %}
</ol>

