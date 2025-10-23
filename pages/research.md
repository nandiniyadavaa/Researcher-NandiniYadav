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
.projects-sub{color:var(--muted);text-align:center;margin:-.4rem auto 1.2rem;max-width:800px}
.filters{display:flex;gap:10px;flex-wrap:wrap;justify-content:center;margin:10px 0 20px}
.filter-btn{border:1px solid var(--ring);background:#f7f8fb;border-radius:999px;padding:7px 14px;
  font-weight:600;cursor:pointer;transition:background .2s,border-color .2s,color .2s}
.filter-btn:focus{outline:2px solid #cfe0ff;outline-offset:2px}
.filter-btn.active{background:#eaf2fd;color:var(--ink);border-color:#cfe0ff}
.grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:18px}
@media (max-width:980px){.grid{grid-template-columns:repeat(2,1fr)}}
@media (max-width:620px){.grid{grid-template-columns:1fr}}
.card{background:var(--card);border:1px solid var(--ring);border-radius:12px;overflow:hidden;transition:box-shadow .2s,transform .1s}
.card:hover{box-shadow:0 8px 24px rgba(13,62,169,.12);transform:translateY(-1px)}
.thumbless{height:8px;width:100%;background:linear-gradient(90deg,#eaf2fd,#dbeafe,#c7f9e9)}
.body{padding:14px 16px 16px}
.h{margin:2px 0 6px;font-weight:700;color:#0d3ea9;font-size:1.05rem}
.meta{display:flex;gap:10px;flex-wrap:wrap;margin:0 0 8px;color:var(--muted);font-size:.92rem}
.tag{border:1px solid var(--ring);border-radius:999px;padding:2px 8px;font-size:.82rem}
.p{color:#222;line-height:1.55;margin:0}
.links{display:flex;gap:12px;margin-top:10px}
.links a{color:var(--ink);text-decoration:underline}
.badges{display:flex;gap:6px;flex-wrap:wrap;margin:8px 0 0}
</style>

<div class="projects-wrap">
  <h1 class="projects-title">Research Projects</h1>
  <p class="projects-sub">
    Ongoing and past work across divertor/edge physics, spectroscopy, impurities, and power exhaust.
    Use the filters to explore by theme.
  </p>

  <!-- Filters (keep in sync with tag names used in YAML) -->
  <div class="filters" id="filters" role="tablist" aria-label="Project filters">
    <button class="filter-btn active" data-tag="all" role="tab" aria-selected="true">All</button>
    <button class="filter-btn" data-tag="detachment" role="tab" aria-selected="false">Detachment</button>
    <button class="filter-btn" data-tag="spectroscopy" role="tab" aria-selected="false">Spectroscopy</button>
    <button class="filter-btn" data-tag="impurities" role="tab" aria-selected="false">Impurities</button>
    <button class="filter-btn" data-tag="diagnostics" role="tab" aria-selected="false">Diagnostics</button>
    <button class="filter-btn" data-tag="modeling" role="tab" aria-selected="false">Modeling</button>
    <button class="filter-btn" data-tag="low-temperature plasma" role="tab" aria-selected="false">Low-Temperature Plasma</button>
    <button class="filter-btn" data-tag="recycling" role="tab" aria-selected="false">Recycling</button>
  </div>

  <!-- Grid -->
  <div class="grid" id="grid">
    {% assign items = site.data.research_overview %}
    {% for item in items %}
      <article class="card" data-tags="{{ item.tags | join: ',' }}">
        <div class="thumbless"></div>
        <div class="body">
          <div class="h">{{ item.title }}</div>
          <div class="meta">
            {% if item.years and item.years != '' %}<span class="tag">{{ item.years }}</span>{% endif %}
            {% if item.org and item.org != '' %}<span class="tag">{{ item.org }}</span>{% endif %}
          </div>
          <p class="p">{{ item.blurb }}</p>

          <div class="badges">
            {% for t in item.tags %}<span class="tag">{{ t }}</span>{% endfor %}
          </div>

          {% if item.links %}
          <div class="links">
            {% for k in item.links %}
              {% if k[1] and k[1] != '' %}
                <a href="{{ k[1] }}" target="_blank" rel="noopener">{{ k[0] | capitalize }}</a>
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
/* Accessible multi-word tag filter with comma-separated data-tags */
(function() {
  const btns = Array.from(document.querySelectorAll('.filter-btn'));
  const cards = Array.from(document.querySelectorAll('.card'));

  function normTags(el){ return (el.getAttribute('data-tags')||'').split(',').map(s=>s.trim()).filter(Boolean); }
  function setActive(btn){ btns.forEach(b=>{ const on=b===btn; b.classList.toggle('active',on); b.setAttribute('aria-selected', on?'true':'false'); }); }
  function apply(tag){ cards.forEach(c=> c.style.display = (tag==='all'||normTags(c).includes(tag)) ? '' : 'none'); }

  btns.forEach(btn=>{
    btn.addEventListener('click', ()=>{ setActive(btn); apply(btn.dataset.tag); });
    btn.addEventListener('keydown', e=>{ if(e.key==='Enter'||e.key===' '){ e.preventDefault(); btn.click(); }});
  });
})();
</script>
