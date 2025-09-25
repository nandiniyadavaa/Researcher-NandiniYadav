---
title: Research
layout: default
permalink: /research
---

<style>
/* ====== Projects page ====== */
:root{
  --page-w: 1100px;
  --ink:#0d3ea9; --ink-2:#1a4fa3; --muted:#6b7280;
  --card:#fff; --bg:transparent; --ring:#e6e6e6;
}

.projects-wrap{max-width:var(--page-w);margin:0 auto;padding:0 1rem 2rem}
.projects-title{text-align:center;font-weight:700;letter-spacing:.2px;margin:.2rem 0 1.2rem;
  font-size:clamp(1.8rem,2.6vw,2.2rem);color:var(--ink-2)}
.projects-sub{color:var(--muted);text-align:center;margin:-.4rem auto 1.2rem;max-width:800px}

/* filter bar */
.filters{display:flex;gap:10px;flex-wrap:wrap;justify-content:center;margin:10px 0 20px}
.filter-btn{border:1px solid var(--ring);background:#f7f8fb;border-radius:999px;padding:7px 14px;
  font-weight:600;cursor:pointer}
.filter-btn.active{background:#eaf2fd;color:var(--ink);border-color:#cfe0ff}

/* grid */
.grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:18px}
@media (max-width:980px){.grid{grid-template-columns:repeat(2,1fr)}}
@media (max-width:620px){.grid{grid-template-columns:1fr}}

/* card */
.card{background:var(--card);border:1px solid var(--ring);border-radius:12px;overflow:hidden;
  transition:box-shadow .2s, transform .1s}
.card:hover{box-shadow:0 8px 24px rgba(13,62,169,.12);transform:translateY(-1px)}

/* header strip used when no image */
.thumbless{
  height:8px; width:100%;
  background: linear-gradient(90deg,#eaf2fd,#dbeafe,#c7f9e9);
}

/* body */
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
    A selection of ongoing and past projects in divertor/edge physics, spectroscopy, and power exhaust.
    Use the filters to explore by theme.
  </p>

  <!-- Filters -->
  <div class="filters" id="filters">
    <button class="filter-btn active" data-tag="all">All</button>
    <button class="filter-btn" data-tag="detachment">Detachment</button>
    <button class="filter-btn" data-tag="spectroscopy">Spectroscopy</button>
    <button class="filter-btn" data-tag="impurities">Impurities</button>
    <button class="filter-btn" data-tag="diagnostics">Diagnostics</button>
    <button class="filter-btn" data-tag="modeling">Modeling</button>
  </div>

  <!-- Grid -->
  <div class="grid" id="grid">

    <!-- CARD 1 -->
    <article class="card" data-tags="detachment spectroscopy diagnostics">
      <div class="thumbless"></div>
      <div class="body">
        <div class="h">Balmer Spectroscopy of Divertor Detachment (DIII-D)</div>
        <div class="meta"><span class="tag">2024–</span><span class="tag">DIII-D</span></div>
        <p class="p">Separate excitation vs. recombination contributions in Balmer lines to quantify
          particle sources/sinks and onset of EIR/MAR; connect to heat-flux reduction and control.</p>
        <div class="badges"><span class="tag">detachment</span><span class="tag">spectroscopy</span></div>
        <div class="links">
          <a href="#">Summary</a><a href="#">Slides</a><a href="#">Preprint</a>
        </div>
      </div>
    </article>

    <!-- CARD 2 -->
    <article class="card" data-tags="diagnostics spectroscopy">
      <div class="thumbless"></div>
      <div class="body">
        <div class="h">Edge Optical Diagnostics: Design &amp; Calibration</div>
        <div class="meta"><span class="tag">2023–</span><span class="tag">DIII-D</span></div>
        <p class="p">Commission line-of-sight and imaging systems, absolute calibration, and uncertainty
          pipelines for multi-campaign analysis.</p>
        <div class="badges"><span class="tag">diagnostics</span></div>
        <div class="links"><a href="#">Methods</a></div>
      </div>
    </article>

    <!-- CARD 3 -->
    <article class="card" data-tags="impurities detachment">
      <div class="thumbless"></div>
      <div class="body">
        <div class="h">Impurity &amp; Neutral Dynamics Near the X-Point</div>
        <div class="meta"><span class="tag">2022–</span><span class="tag">DIII-D</span></div>
        <p class="p">Assess impurity screening vs. leakage and the role of molecule-assisted processes for
          reactor-relevant power exhaust.</p>
        <div class="badges"><span class="tag">impurities</span><span class="tag">detachment</span></div>
        <div class="links"><a href="#">Poster</a></div>
      </div>
    </article>

    <!-- CARD 4 -->
    <article class="card" data-tags="spectroscopy modeling">
      <div class="thumbless"></div>
      <div class="body">
        <div class="h">Spectral Inversion &amp; Tomography for Line-Integrated Views</div>
        <div class="meta"><span class="tag">2021–</span><span class="tag">DIII-D</span></div>
        <p class="p">From chords to fields: physics-aware inversions to recover emissivity and
          recombination fronts consistent with transport models.</p>
        <div class="badges"><span class="tag">modeling</span><span class="tag">spectroscopy</span></div>
        <div class="links"><a href="#">Code</a></div>
      </div>
    </article>

    <!-- CARD 5 -->
    <article class="card" data-tags="diagnostics">
      <div class="thumbless"></div>
      <div class="body">
        <div class="h">ADITYA-U: Recycling &amp; Temperature from Visible Lines</div>
        <div class="meta"><span class="tag">2019–2021</span><span class="tag">ADITYA-U</span></div>
        <p class="p">Visible spectroscopy and imaging to study wall recycling, impurity influx, and edge temperature trends.</p>
        <div class="badges"><span class="tag">diagnostics</span></div>
        <div class="links"><a href="#">Paper</a></div>
      </div>
    </article>

  </div>
</div>

<script>
/* simple tag filter */
const buttons=[...document.querySelectorAll('.filter-btn')];
const cards=[...document.querySelectorAll('.card')];
buttons.forEach(b=>b.addEventListener('click',()=>{
  buttons.forEach(x=>x.classList.remove('active')); b.classList.add('active');
  const tag=b.dataset.tag;
  cards.forEach(c=>{
    const have = c.dataset.tags.split(' ');
    c.style.display = (tag==='all'||have.includes(tag)) ? '' : 'none';
  });
}));
</script>
