---
title: Contact
layout: default
permalink: /contact/
---

<style>
  /* widen only THIS page's content box */
.page-content .wrapper{
  max-width: 1200px;     /* wider page container */
  padding-left: 16px;
  padding-right: 16px;
}

/* center the hero card; no funky width tricks */
.contact-hero{
  margin: 0 auto 28px;
  max-width: 1100px;     /* the card itself */
  border-radius: 22px;
  overflow: hidden;
}

/* layout: photo + info */
.contact-grid{
  display: grid;
  grid-template-columns: 360px minmax(0,1fr);  /* minmax prevents overflow */
  gap: 28px;
  align-items: start;
}
@media (max-width: 980px){
  .contact-grid{ grid-template-columns: 1fr; }
}

/* make sure images can’t push layout wider */
img{ max-width:100%; height:auto; }

/* optional: slightly smaller title to avoid long wrap */
.contact-info h1{
  font-size: clamp(1.6rem, 2.2vw, 2.2rem);
  line-height: 1.2;
  overflow-wrap: anywhere;
}

/* Simple, tidy contact layout */
.contact {
  max-width: 980px; margin: 0 auto 2.5rem; padding: 0 1rem;
  display: grid; grid-template-columns: 320px 1fr; gap: 28px; align-items: start;
}
@media (max-width: 900px){ .contact { grid-template-columns: 1fr; } }

.contact .photo img {
  width: 100%; height: auto; display: block; border-radius: 12px;
  box-shadow: 0 4px 18px rgba(0,0,0,.08);
}

h1.contact-title { margin: .25rem 0 .5rem; font-size: clamp(1.6rem, 2.2vw, 2.1rem); }
.contact-sub { color: #6b7280; margin: 0 0 1rem; }

.kv { display: grid; grid-template-columns: 140px 1fr; gap: 10px 18px; }
.kv div:first-child { color:#6b7280; font-weight:600; }
.kv a { color: inherit; text-decoration: underline dotted; text-underline-offset: 2px; }

.cards { display: grid; gap: 16px; grid-template-columns: repeat(2, minmax(0,1fr)); margin-top: 16px; }
@media (max-width: 600px){ .cards { grid-template-columns: 1fr; } }
.card { border: 1px solid #e5e7eb; border-radius: 10px; padding: 14px; }
.card h3 { margin: 0 0 .4rem; font-size: 1rem; }

.links { display:flex; gap:18px; flex-wrap:wrap; margin-top: 10px; }
.links a { border:1px solid #e5e7eb; border-radius: 999px; padding:6px 12px; }
</style>

<div class="contact">
  <!-- Left: Photo -->
  <div class="photo">
    <!-- Put your picture at /assets/image/contact.jpg -->
    <img src="{{ site.baseurl }}/assets/image/Nandini_Yadava.jpg" alt="Dr. Nandini Yadav (Yadava)">
  </div>

  <!-- Right: Info -->
  <div>
    <h1 class="contact-title">Dr. Nandini Yadava (Yadav)</h1>
    <p class="contact-sub">Postdoctoral Researcher · DIII-D National Fusion Facility (General Atomics)</p>

    <div class="kv">
      <div>Phone</div>
      <div>
        <a href="tel:+18587174976">+1-858-717-4976 (M)</a>
        <a href="tel:+18584554748">+1-858-455-4748 (O)</a>
      </div>

      <div>Email</div>
      <div>
        <a href="mailto:nandini7754@gmail.com">nandini7754@gmail.com</a>
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
  </div>
</div>
