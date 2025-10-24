---
title: Research
layout: default
permalink: /research
---

<style>
:root{ --page-w:1100px; --ink:#0d3ea9; --ink-2:#1a4fa3; --muted:#6b7280; --card:#fff; --ring:#e6e6e6; }
.projects-wrap{max-width:var(--page-w);margin:0 auto;padding:0 1rem 2rem}
.projects-title{text-align:center;font-weight:700;letter-spacing:.2px;margin:.2rem 0 1.2rem;
  font-size:clamp(1.8rem,2.6vw,2.2rem);color:var(--ink-2)}
.projects-sub{color:var(--muted);text-align:center;margin:-.4rem auto 1.2rem;max-width:860px}

/* filters */
.filters{display:flex;gap:10px;flex-wrap:wrap;justify-content:center;margin:10px 0 20px}
.filter-btn{border:1px solid var(--ring);background:#f7f8fb;border-radius:999px;padding:7px 14px;
  font-weight:600;cursor:pointer;transition:background .2s,border-color .2s,color .2s}
.filter-btn:focus{outline:2px solid #cfe0ff;outline-offset:2px}
.filter-btn.active{background:#eaf2fd;color:#0d3ea9;border-color:#cfe0ff}

/* horizontal list with thumbnail */
.list{display:flex;flex-direction:column;gap:14px}
.card{display:flex;gap:0;align-items:stretch;background:var(--card);border:1px solid var(--ring);
  border-radius:12px;overflow:hidden;transition:box-shadow .2s,transform .1s}
.card:hover{box-shadow:0 8px 24px rgba(13,62,169,.12);transform:translateY(-1px)}

/* thumbnail column */
.thumb-wrap{position:relative;flex:0 0 220px;max-width:220px;background:#f5f7fb}
.thumb{width:100%;height:100%;aspect-ratio:16/11;object-fit:cover;display:block}
.thumb-fallback{width:100%;height:100%;min-height:150px;background:
  linear-gradient(135deg,#eaf2fd,#dbeafe 60%,#c7f9e9)}

/* text column */
.body{padding:14px 16px 16px;flex:1;min-width:0}
.h{margin:0 0 6px;font-weight:700;color:#0d3ea9;font-size:1.08rem;line-height:1.25}
.meta{display:flex;gap:10px;flex-wrap:wrap;margin:0 0 8px;color:var(--muted);font-size:.92rem}
.tag{border:1px solid var(--ring);border-radius:999px;padding:2px 8px;font-size:.82rem;background:#fff}
.p{color:#222;line-height:1.6;margin:0}
.badges{display:flex;gap:6px;flex-wrap:wrap;margin:10px 0 0}
.links{display:flex;gap:12px;margin-top:10px;flex-wrap:wrap}
.links a{color:#0d3ea9;text-decoration:underline;white-space:nowrap}

/* responsive */
@media (max-width:860px){ .thumb-wrap{flex-basis:180px;max-width:180px} }
@media (max-width:640px){
  .card{flex-direction:column}
  .thumb-wrap{flex-basis:auto;max-width:none}
  .thumb,.thumb-fallback{aspect-ratio:16/9;min-height:160px}
  .body{padding:12px 14px 14px}
}
</style>

<div class="projects-wrap">
  <h1 class="projects-title">Research Projects</h1>
  <p class="projects-sub">
    Ongoing and past work across divertor/edge physics, spectroscopy, impurities, recycling, and power exhaust.
    Use the filters to explore by theme.
  </p>

  <!-- Filters -->
  <div class="filters" id="filters" role="tablist" aria-label="Project filters">
    <button class="filter-btn active" data-tag="all" role="tab" aria-selected="true">All</button>
    <button class="filter-btn" data-tag="detachment" role="tab" aria-selected="false">Detachment</button>
    <button class="filter-btn" data-tag="spectroscopy" role="tab" aria-selected="false">Spectroscopy</button>
    <button class="filter-btn" data-tag="impurities" role="tab" aria-selected="false">Impurities</button>
    <button class="filter-btn" data-tag="recycling" role="tab" aria-selected="false">Recycling</button>
    <button class="filter-btn" data-tag="diagnostics" role="tab" aria-selected="false">Diagnostics</button>
    <button class="filter-btn" data-tag="modeling" role="tab" aria-selected="false">Modeling</button>
    <button class="filter-btn" data-tag="low-temperature plasma" role="tab" aria-selected="false">Low-Temperature Plasma</button>
  </div>

  <!-- Horizontal list -->
  <div class="list" id="list">
    {% assign items = site.data.research_overview %}
    {% for item in items %}
      <article class="card" data-tags="{{ item.tags | default: empty | join: ',' }}">
        <div class="thumb-wrap">
          {% if item.image and item.image != '' %}
            <img class="thumb" src="{{ item.image | relative_url }}" alt="{{ item.alt | default: item.title }}">
          {% else %}
            <div class="thumb-fallback" aria-hidden="true"></div>
          {% endif %}
        </div>

        <div class="body">
          <div class="h">{{ item.title }}</div>
          <div class="meta">
            {% if item.years and item.years != '' %}<span class="tag">{{ item.years }}</span>{% endif %}
            {% if item.org and item.org != '' %}<span class="tag">{{ item.org }}</span>{% endif %}
          </div>

          <p class="p">{{ item.blurb }}</p>

          <div class="badges">
            {% if item.tags %}
              {% for t in item.tags %}
                <span class="tag">{{ t }}</span>
              {% endfor %}
            {% endif %}
          </div>

          {% if item.links %}
            <div class="links">
              {% for pair in item.links %}
                {% assign label = pair[0] %}
                {% assign url   = pair[1] %}
                {% if url and url != '' %}
                  <a href="{{ url }}" target="_blank" rel="noopener">{{ label | capitalize }}</a>
                {% endif %}
              {% endfor %}
            </div>
          {% endif %}
        </div>
      </article>
    {% endfor %}
  </div>
</div>

<script>
/* Tag filter (comma-separated data-tags on cards) */
(function() {
  const btns = Array.from(document.querySelectorAll('.filter-btn'));
  const cards = Array.from(document.querySelectorAll('.card'));
  const tagsOf = el => (el.getAttribute('data-tags')||'').split(',').map(s=>s.trim()).filter(Boolean);

  function setActive(btn){
    btns.forEach(b=>{
      const on = b===btn;
      b.classList.toggle('active', on);
      b.setAttribute('aria-selected', on ? 'true' : 'false');
    });
  }
  function apply(tag){
    cards.forEach(c => {
      const have = tagsOf(c);
      c.style.display = (tag==='all' || have.includes(tag)) ? '' : 'none';
    });
  }
  btns.forEach(btn=>{
    btn.addEventListener('click', ()=>{ setActive(btn); apply(btn.dataset.tag); });
    btn.addEventListener('keydown', e=>{ if(e.key==='Enter'||e.key===' '){ e.preventDefault(); btn.click(); }});
  });
})();
</script>

/* === Force rectangular thumbnails (no oval, no rounding) === */
.thumb-wrap,
.thumb {
  border-radius: 0 !important;   /* kill any rounding */
  clip-path: none !important;     /* avoid accidental masking */
}

/* Make the image fill a rectangular box without distortion */
.thumb-wrap { 
  flex: 0 0 240px;                /* pick a width for the left column */
  max-width: 240px;
  height: 160px;                  /* fixed rectangle (adjust as you like) */
  background: #f5f7fb;
}
.thumb {
  width: 100%;
  height: 100%;
  object-fit: cover;              /* crop to fit the rectangle */
  aspect-ratio: auto !important;  /* disable any earlier aspect-ratio */
}

/* Optional: if you also don’t want rounded cards at all */
.card { border-radius: 0 !important; }

