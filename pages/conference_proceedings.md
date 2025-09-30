---
title: Conference Proceedings
layout: default
permalink: /conference-proceedings
---

# Conference Proceedings

# Conference Proceedings

<ol class="pub-list">
{% for pub in site.data.publications_oral %}
  <li class="pub-item">
    <div class="pub-title"><em>{{ pub.title }}</em></div>
    <div class="pub-authors">{{ pub.authors }}</div>

    {%- assign meta = "" -%}
    {%- if pub.venue -%}
      {%- assign meta = pub.venue -%}
    {%- endif -%}

    {%- if pub.location -%}
      {%- if meta != "" -%}{%- assign meta = meta | append: ", " -%}{%- endif -%}
      {%- assign meta = meta | append: pub.location -%}
    {%- endif -%}

    {%- if pub.year -%}
      {%- if meta != "" -%}{%- assign meta = meta | append: ", " -%}{%- endif -%}
      {%- assign meta = meta | append: pub.year -%}
    {%- endif -%}

    {%- if pub.session -%}
      {%- if meta != "" -%}{%- assign meta = meta | append: " — " -%}{%- endif -%}
      {%- assign meta = meta | append: "Session " | append: pub.session -%}
    {%- endif -%}

    {%- if pub.link -%}
      {%- if meta != "" -%}{%- assign meta = meta | append: " • " -%}{%- endif -%}
      {%- assign meta = meta | append: '<a href="' | append: pub.link | append: '">link</a>' -%}
    {%- endif -%}

    {%- if pub.note -%}
      {%- if meta != "" -%}{%- assign meta = meta | append: " • " -%}{%- endif -%}
      {%- assign meta = meta | append: pub.note -%}
    {%- endif -%}

    <div class="pub-meta">{{ meta }}</div>
  </li>
{% endfor %}
</ol>

