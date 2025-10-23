---
title: Publications
layout: default
permalink: /publications
---

# Publications

<style>
/* Simple dropdown styling (safe for GitHub Pages) */
.pub-accordion details {
  border: 1px solid #e5e7eb; /* Tailwind gray-200-ish */
  border-radius: 8px;
  margin: 0 0 14px 0;
  padding: 0.25rem 0.75rem 0.75rem 0.75rem;
  background: #fff;
}
.pub-accordion summary {
  cursor: pointer;
  list-style: none; /* hide default marker in some browsers */
  font-weight: 600;
  font-size: 1.1rem;
  padding: 0.25rem 0;
  display: flex;
  align-items: center;
  gap: .5rem;
}
.pub-accordion summary::-webkit-details-marker { display: none; }
.pub-accordion .caret {
  transition: transform .2s ease;
  display: inline-block;
}
.pub-accordion details[open] .caret {
  transform: rotate(90deg);
}
.pub-list { margin: .25rem 0 .25rem 1.25rem; }
.pub-item { margin-bottom: .75rem; }
.pub-title a { text-decoration: none; }
.pub-title em { font-style: italic; }
.pub-authors { color: #374151; /* gray-700 */ font-size: .95rem; margin-top: .2rem; }
.pub-meta { color: #6b7280; /* gray-500 */ font-size: .9rem; margin-top: .2rem; }
</style>

<div class="pub-accordion">

<!-- ===================== Planned submissions ===================== -->
<details>
  <summary><span class="caret">▶</span> Planned submissions</summary>
  <ol class="pub-list">
  {% for pub in site.data.publications_recent %}
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
</details>

<!-- ===================== Peer-Reviewed Articles ===================== -->
<details>
  <summary><span class="caret">▶</span> Peer-Reviewed Articles</summary>
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
</details>

<!-- ===================== Conference Proceedings ===================== -->
<details>
  <summary><span class="caret">▶</span> Conference Proceedings</summary>
  <ol class="pub-list">
  {% for pub in site.data.publications_conference %}
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
</details>

<!-- ===================== Oral Presentations ===================== -->
<details>
  <summary><span class="caret">▶</span> Oral Presentations</summary>
  <ol class="pub-list">
  {% for pub in site.data.publications_oral %}
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
</details>

<!-- ===================== Poster Presentations ===================== -->
<details>
  <summary><span class="caret">▶</span> Poster Presentations</summary>
  <ol class="pub-list">
  {% for pub in site.data.publications_poster %}
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
</details>

</div>
