---
title: Contact
layout: default
permalink: /contact/
---

<style>
/* Simple, tidy contact layout */
.contact{
  max-width:980px; margin:0 auto 2.5rem; padding:0 1rem;
  display:grid; grid-template-columns:420px 1fr; gap:28px; align-items:start;
}
@media (max-width:900px){ .contact{ grid-template-columns:1fr; } }

.contact .photo img{ width:100%; height:auto; display:block; border-radius:12px; box-shadow:none; }

h1.contact-title{ margin:.25rem 0 .5rem; font-size:clamp(1.6rem,2.2vw,2.1rem); }
.contact-sub{ color:#6b7280; margin:0 0 1rem; }

.kv{ display:grid; grid-template-columns:140px 1fr; gap:10px 18px; }
.kv div:first-child{ color:#6b7280; font-weight:600; }
.kv a{ text-decoration:underline; text-underline-offset:2px; }

/* cards below the separator */
.cards{ display:grid; gap:16px; grid-template-columns:repeat(2,minmax(0,1fr)); margin-top:16px; }
@media (max-width:600px){ .cards{ grid-template-columns:1fr; } }
.card{ border:none; }
.card h3{ margin:0 0 .4rem; font-size:1rem; }

/* styled horizontal rule */
.section-line{ border:0; height:2px; background:#ddd; margin:28px 0 20px; }
</style>

<div class="contact">
  <!-- Left: Photo -->
  <div class="photo">
    <img src="{{ site.baseurl }}/assets/image/Nandini_Yadava.jpg" alt="Dr. Nandini Yadav (Yadava)">
  </div>

  <!-- Right: Info -->
  <div>
    <h1 class="contact-title">Dr. Nandini Yadava (Yadav)</h1>
    <p class="contact-sub">Postdoctoral Researcher</p>
    <p class="contact-sub">DIII-D National Fusion Facility (General Atomics)</p>

    <div class="kv">
      <div>Phone</div>
      <div>
        <a href="tel:+18587174976">+1-858-717-4976 (M)</a> ·
        <a href="tel:+18584554748">+1-858-455-4748 (O)</a>
      </div>

      <div>Email</div>
      <div>
        <a href="mailto:nandini7754@gmail.com">nandini7754@gmail.com</a> ·
        <a href="mailto:yadavn@fusion.gat.com">yadavn@fusion.gat.com</a>
      </div>

      <div>Address</div>
      <div>
        <a href="https://maps.google.com/?q=3550+General+Atomics+Court,+San+Diego,+CA+92121" target="_blank" rel="noopener">
          General Atomics 13-460, 3550 General Atomics Ct, San Diego, CA 92121
        </a>
      </div>

      <div>Date of birth</div>
      <div>15 July 1993</div>

      <div>ORCID</div>
      <div><a href="https://orcid.org/0000-0001-5522-2450">0000-0001-5522-2450</a></div>
    </div>
  </div>
</div>

<hr class="section-line">

## Next section title

<div class="cards">
  <div class="card">
    <h3>Academic IDs</h3>
    <div class="links">
      <a href="https://scholar.google.com/" target="_blank">Google Scholar</a>
      <a href="https://www.researchgate.net/" target="_blank">ResearchGate</a>
      <a href="https://publons.com/" target="_blank">Publons</a>
    </div>
  </div>
  <div class="card">
    <h3>Focus</h3>
    <p>Divertor detachment · Balmer spectroscopy · AM processes (EIR/MAR)</p>
  </div>
</div>
