---
title: Contact
layout: default
permalink: /contact/
---

<style>
/* ====== "Extraordinary" contact page (self-contained) ====== */
:root{
  --bg: #0b0d14;
  --panel: rgba(255,255,255,.06);
  --text: #e6e9ef;
  --muted: #aab1bd;
  --brand1:#84a3ff; --brand2:#7ef1d1; --brand3:#f7a6ff;
  --glow: 0 10px 30px rgba(132,163,255,.35), 0 0 60px rgba(126,241,209,.2);
}
@media (prefers-color-scheme: light){
  :root{ --bg:#f7f8fb; --panel:rgba(0,0,0,.04); --text:#0b0d14; --muted:#4a5568; }
}
body .page-content{ background:
  radial-gradient(1000px 600px at 100% -10%, rgba(132,163,255,.18), transparent 55%),
  radial-gradient(900px 600px at -10% 110%, rgba(126,241,209,.18), transparent 55%);}

/* hero frame */
.contact-hero{
  position:relative; isolation:isolate;
  border-radius:22px; padding:28px; margin:0 0 28px 0;
  background: linear-gradient(135deg, rgba(255,255,255,.08), rgba(255,255,255,.02));
  overflow:hidden;
}
.contact-hero:before{
  content:""; position:absolute; inset:-2px;
  background: conic-gradient(from 180deg, var(--brand1), var(--brand2), var(--brand3), var(--brand1));
  filter: blur(16px); opacity:.55; z-index:-2;
}
.contact-hero:after{
  content:""; position:absolute; inset:1px; border-radius:20px;
  background: linear-gradient(180deg, rgba(255,255,255,.9), rgba(255,255,255,.04));
  mix-blend-mode:overlay; opacity:.3; z-index:-1;
}

/* layout */
.contact-grid{
  display:grid; gap:28px;
  grid-template-columns: 320px 1fr;
  align-items: start;
}
@media (max-width: 900px){ .contact-grid{ grid-template-columns: 1fr; } }

/* avatar card */
.contact-avatar{
  position:relative; padding:22px; border-radius:18px;
  backdrop-filter: blur(10px); background:var(--panel);
  box-shadow: var(--glow);
}
.contact-avatar .imgwrap{
  aspect-ratio: 1 / 1; border-radius:18px; overflow:hidden; position:relative;
}
.contact-avatar img{ width:100%; height:100%; object-fit:cover; display:block; }
.badge{
  position:absolute; right:12px; bottom:12px;
  background: linear-gradient(135deg, var(--brand2), var(--brand1));
  color:#051016; font-weight:700; padding:6px 10px; border-radius:10px; font-size:.8rem;
  box-shadow: 0 6px 20px rgba(0,0,0,.25);
}

/* info card */
.contact-info{
  padding:22px; border-radius:18px; backdrop-filter: blur(10px);
  background:var(--panel);
}
.contact-info h1{ margin:.1rem 0 .35rem 0; font-size: clamp(1.6rem, 2.4vw, 2.2rem); }
.contact-info .subtitle{ color:var(--muted); margin:.2rem 0 1rem 0; }

.kv{
  display:grid; grid-template-columns: 140px 1fr; gap:10px 18px; align-items:baseline;
}
.kv div:first-child{ color:var(--muted); font-weight:600; letter-spacing:.02em; }
.kv a{ color:inherit; text-decoration: none; border-bottom:1px dotted rgba(255,255,255,.25); }
.kv a:hover{ border-bottom-color: transparent; }

.chips{ display:flex; flex-wrap:wrap; gap:10px; margin-top:14px; }
.chip{
  --c: var(--brand1);
  border:1px solid color-mix(in oklab, var(--c) 60%, transparent);
  background: linear-gradient(180deg, color-mix(in oklab, var(--c) 12%, transparent), transparent);
  color:var(--text);
  padding:6px 10px; border-radius:999px; font-size:.85rem; display:inline-flex; gap:8px; align-items:center;
  transition: transform .15s ease, box-shadow .15s ease;
}
.chip:hover{ transform: translateY(-2px); box-shadow: var(--glow); }
.chip svg{ width:16px; height:16px; }

.panels{ display:grid; gap:22px; grid-template-columns: repeat(3, 1fr); margin-top:22px;}
@media (max-width: 900px){ .panels{ grid-template-columns:1fr; } }
.panel{
  padding:18px; border-radius:16px; background:var(--panel); backdrop-filter: blur(6px);
}
.panel h3{ margin:0 0 .6rem 0; font-size:1.05rem; }
.panel p{ margin:.3rem 0; }

/* QR grid */
.qrgrid{ display:flex; gap:24px; flex-wrap:wrap; justify-content:center; }
.qrcard{ text-align:center; }
.qrcard img{
  width:160px; height:160px; object-fit:contain; background:#fff; padding:8px;
  border-radius:14px; box-shadow:0 2px 12px rgba(0,0,0,.12);
}
.print-note{ color:var(--muted); font-size:.9rem; }
@media print{
  .contact-hero{ box-shadow:none; }
  .chip, .badge{ box-shadow:none; }
}
</style>

<div class="contact-hero">
  <div class="contact-grid">
    <!-- LEFT: avatar -->
    <div class="contact-avatar">
      <div class="imgwrap">
        <!-- update the image path -->
        <img src="{{ site.baseurl }}/assets/image/Nandini_Yadava.jpg" alt="Dr. Nandini Yadav (Yadava)">
        <span class="badge">Available for collab</span>
      </div>

      <div class="chips" style="margin-top:14px">
        <a class="chip" style="--c:var(--brand2)" href="mailto:nandini7754@gmail.com" title="Email">
          <!-- mail icon -->
          <svg viewBox="0 0 24 24" fill="none"><path d="M4 6h16a1 1 0 0 1 1 1v10a1 1 0 0 1-1 1H4a1 1 0 0 1-1-1V7a1 1 0 0 1 1-1zm0 0 8 6 8-6" stroke="currentColor" stroke-width="1.6" stroke-linecap="round"/></svg>
          Email me
        </a>
        <a class="chip" style="--c:var(--brand1)" href="tel:+18587174976">
          <!-- phone icon -->
          <svg viewBox="0 0 24 24" fill="none"><path d="M6.6 3.6 9 3l2 4-2.2 1.4a14 14 0 0 0 6.8 6.8L17 13l4 2-0.6 2.4c-.3 1-1.3 1.6-2.3 1.4A17.8 17.8 0 0 1 3.2 6c-.2-1 .4-2 1.4-2.3z" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg>
          Call
        </a>
        <a class="chip" style="--c:var(--brand3)" href="https://orcid.org/0000-0001-5522-2450" target="_blank" rel="noopener">
          <!-- link icon -->
          <svg viewBox="0 0 24 24" fill="none"><path d="M10 13a5 5 0 1 1 4 4l-6 6H4v-4l6-6z" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg>
          ORCID
        </a>
      </div>
    </div>

    <!-- RIGHT: info -->
    <div class="contact-info">
      <h1>Dr. Nandini Yadav (Yadava)</h1>
      <div class="subtitle">Postdoctoral Researcher · DIII-D National Fusion Facility (General Atomics)</div>

      <div class="kv">
        <div>Phone</div>
        <div><a href="tel:+18587174976">+1-858-717-4976 (M)</a> &nbsp; · &nbsp; <a href="tel:+18584554748">+1-858-455-4748 (O)</a></div>

        <div>Email</div>
        <div><a href="mailto:nandini7754@gmail.com">nandini7754@gmail.com</a> · <a href="mailto:yadavn@fusion.gat.com">yadavn@fusion.gat.com</a></div>

        <div>Address</div>
        <div>General Atomics 13-460, 3550 General Atomics Court, San Diego, CA 92121</div>

        <div>Date of birth</div>
        <div>15 July 1993</div>

        <div>ORCID</div>
        <div><a href="https://orcid.org/0000-0001-5522-2450">0000-0001-5522-2450</a></div>
      </div>

      <div class="panels">
        <div class="panel">
          <h3>Academic IDs</h3>
          <p><a href="https://scholar.google.com/" target="_blank" rel="noopener">Google Scholar</a></p>
          <p><a href="https://www.researchgate.net/" target="_blank" rel="noopener">ResearchGate</a></p>
          <p><a href="https://publons.com/" target="_blank" rel="noopener">Publons</a></p>
        </div>
        <div class="panel">
          <h3>Primary Focus</h3>
          <p>Divertor detachment · Balmer spectroscopy · AM processes (EIR/MAR)</p>
        </div>
        <div class="panel">
          <h3>Available For</h3>
          <p>Collaborations · Seminars · Review requests</p>
          <p class="print-note">Prefer email for the first contact.</p>
        </div>
      </div>
    </div>
  </div>
</div>

## Quick Links (QR)
<div class="qrgrid">
  <div class="qrcard">
    <img src="{{ site.baseurl }}/assets/image/qr_researchgate.png" alt="ResearchGate QR">
    <div><a href="https://www.researchgate.net/" target="_blank" rel="noopener">ResearchGate</a></div>
  </div>
  <div class="qrcard">
    <img src="{{ site.baseurl }}/assets/image/qr_scholar.png" alt="Google Scholar QR">
    <div><a href="https://scholar.google.com/" target="_blank" rel="noopener">Google Scholar</a></div>
  </div>
</div>
