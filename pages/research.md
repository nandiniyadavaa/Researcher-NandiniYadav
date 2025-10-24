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

/* list */
.list{display:flex;flex-direction:column;gap:14px}

/* CARD: switch to block flow so image can float and text wraps */
.card{
  display:block;
  background:var(--card);
  border:1px solid var(--ring);
  border-radius:12px;
  overflow:hidden;
  transition:box-shadow .2s,transform .1s;
  padding:12px 14px 14px; /* give room since no flex gutters */
  position:relative;
}
.card:hover{box-shadow:0 8px 24px rgba(13,62,169,.12);transform:translateY(-1px)}
/* clearfix for the float */
.card::after{content:"";display:table;clear:both}

/* THUMBNAIL: float left, keep full image (no crop), allow natural aspect ratio */
.thumb-wrap{
  float:left;
  /* keep it reasonably sized while preserving the image’s own aspect ratio */
  inline-size:clamp(240px, 42%, 420px);
  margin:4px 16px 10px 2px;
  background:#f5f7fb;
  border-radius:10px;
  overflow:hidden; /* just for rounded corners, not cropping aspect */
  /* optional nicer wrap curve */
  shape-outside: inset(0 round 12px);
}
.thumb{
  display:block;
  width:100%;
  height:auto;          /* <- preserve orientation/ratio */
  object-fit:contain;   /* <- never crop */
  border-radius:0;
  clip-path:none;
  background:#f5f7fb;
}
.thumb.contain{object-fit:contain} /* keep your opt-in path working */
.thumb-fallback{width:100%;aspect-ratio:16/9;min-height:160px;background:linear-gradient(135deg,#eaf2fd,#dbeafe 60%,#c7f9e9)}

/* TEXT column becomes normal flow content that wraps around the floated image */
.body{min-width:0}
.h{margin:0 0 6px;font-weight:700;color:#0d3ea9;font-size:1.08rem;line-height:1.25}
.meta{display:flex;gap:10px;flex-wrap:wrap;margin:0 0 8px;color:var(--muted);font-size:.92rem}
.tag{border:1px solid var(--ring);border-radius:999px;padding:2px 8px;font-size:.82rem;background:#fff}
.p{color:#222;line-height:1.6;margin:0}
.badges{display:flex;gap:6px;flex-wrap:wrap;margin:10px 0 0}
.links{display:flex;gap:12px;margin-top:10px;flex-wrap:wrap}
.links a{color:#0d3ea9;text-decoration:underline;white-space:nowrap}

/* responsive: on narrow screens remove float so image stacks above text */
@media (max-width:640px){
  .thumb-wrap{
    float:none;
    inline-size:100%;
    margin:0 0 10px 0;
  }
  .card{padding:12px 12px 14px}
}
  /* Cap tall figures so a single item can't tower over the text */
.thumb-wrap{
  /* previous rules kept */
  max-height: 420px;                 /* cap the float’s height */
  display: flex; align-items: center; justify-content: center; /* center image in box */
}

/* Make the image fit inside the capped box without cropping */
.thumb{
  width: auto; height: auto;         /* use natural aspect */
  max-width: 100%; max-height: 100%; /* shrink to fit the box */
  object-fit: contain;               /* guarantees no crop */
  aspect-ratio: auto;                /* ignore any inherited ratios */
}

/* Optional: if the oversized one is an SVG, enforce the same fit */
.thumb[src$=".svg"]{
  width: auto; height: auto;
  max-width: 100%; max-height: 100%;
}
/* Justified text with smart hyphenation */
.p{
  color:#222; line-height:1.6; margin:0;
  text-align:justify; text-justify:inter-word;
  hyphens:auto; -webkit-hyphens:auto; -ms-hyphens:auto;
}

/* Give thumbnails a subtle box look */
.thumb-wrap{
  float:left;
  inline-size:clamp(240px, 42%, 420px);
  margin:4px 16px 10px 2px;
  background:#f5f7fb;
  border:1px solid var(--ring);
  border-radius:12px;
  overflow:hidden;
  shape-outside: inset(0 round 12px);
  max-height:420px;
  display:flex; align-items:center; justify-content:center;
  padding:6px; /* slight inner breathing room */
}

/* Make image fit inside the capped box without cropping */
.thumb{
  width:auto; height:auto;
  max-width:100%; max-height:100%;
  object-fit:contain; aspect-ratio:auto;
}

/* --- LANDSCAPE MODE: wide figures => horizontal, neatly aligned --- */
.card.is-landscape{
  /* switch from float-wrapping to a tidy two-column layout */
  display:grid;
  grid-template-columns: minmax(260px, 42%) 1fr;
  column-gap:18px;
  align-items:center; /* vertically center image vs text */
  padding:14px 16px 16px; /* a touch more room when gridded */
}
.card.is-landscape .thumb-wrap{
  float:none; /* stop wrapping */
  inline-size:auto;
  margin:0;           /* let grid gap handle spacing */
  max-height:320px;   /* slightly shorter for wide banners */
  padding:8px;        /* keep the framed look */
}
.card.is-landscape .body{min-width:0}

/* Mobile: stack again */
@media (max-width:640px){
  .card.is-landscape{display:block}
  .card.is-landscape .thumb-wrap{
    float:none; inline-size:100%; margin:0 0 10px 0; max-height:360px;
  }
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

  <!-- List -->
  <div class="list" id="list">
    {% assign items = site.data.research_overview %}
    {% for item in items %}
      {% if item.tags %}{% assign tags_attr = item.tags | join: ',' %}{% else %}{% assign tags_attr = '' %}{% endif %}
      <article class="card" data-tags="{{ tags_attr }}">
        <div class="thumb-wrap">
          {% if item.image and item.image != '' %}
            <img class="thumb {% if item.image_fit == 'contain' %}contain{% endif %}"
                 src="{{ item.image | relative_url }}"
                 alt="{{ item.alt | default: item.title }}"
                 loading="lazy">
          {% else %}
            <div class="thumb-fallback" aria-hidden="true"></div>
          {% endif %}
        </div>

        <div class="body">
          <div class="h">{{ item.title }}</div>
          <div class="meta">
            {% if item.years %}<span class="tag">{{ item.years }}</span>{% endif %}
            {% if item.org %}<span class="tag">{{ item.org }}</span>{% endif %}
          </div>

          <div class="p">
            {{ item.blurb | markdownify }}
          </div>

          {% if item.tags %}
          <div class="badges">
            {% for t in item.tags %}<span class="tag">{{ t }}</span>{% endfor %}
          </div>
          {% endif %}

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

<script defer src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

<script>
/* Tag filter (comma-separated data-tags on cards) */
(function() {
  const btns = Array.from(document.querySelectorAll('.filter-btn'));
  const cards = Array.from(document.querySelectorAll('.card'));
  const tagsOf = el => (el.getAttribute('data-tags')||'')
                        .split(',')
                        .map(s=>s.trim())
                        .filter(Boolean);

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
