---
title: About
layout: default
permalink: /
redirect_from:
  - /about
---


<style>
/* ====== Clean About layout (like the screenshot) ====== */
.about-wrap{
  max-width: 1100px; margin: 0 auto; padding: 0 1rem 2rem;
}
.about-title{
  text-align: center; font-size: clamp(1.8rem, 2.6vw, 2.4rem);
  font-weight: 700; letter-spacing:.01em; margin: .2rem 0 1.4rem;
}
.about-grid{
  display:grid; grid-template-columns: 360px 1fr; gap: 28px; align-items:start;
}
@media (max-width: 980px){ .about-grid{ grid-template-columns:1fr; } }

<div class="about-photo">
  <img src="{{ '/assets/image/2401_PUB012535-Nandni_Yadava_2.jpg' | relative_url }}" alt="Nandini Yadava">
</div>

.about-photo img{
  float:left;
  width:360px;
  max-width:40%;
  height:auto;
  margin:0 24px 14px 0;
  border-radius:10px;
  box-shadow:0 2px 10px rgba(0,0,0,.06);
  shape-outside: inset(0 round 10px);
}

/* readable paragraphs like the example */
.about-body p{
  margin: .75rem 0; line-height: 1.7; font-size: 1.02rem; color:#222;
}
.about-body a{ color:#0d3ea9; font-weight:600; text-decoration: underline; }
.about-body strong{ font-weight:700; }
.about-body em{ font-style: italic; }

/* optional subtle divider between main paragraphs and the list below */
.hr-soft{ height:1px; background:#e6e6e6; border:0; margin: 1.4rem 0; }
</style>

<div class="about-wrap">
  <h1 class="about-title">Dr. Nandini Yadava</h1>

  <div class="about-grid">
    <!-- LEFT: Photo -->
    <div class="about-photo">
      <!-- Put your image here -->
      <img src="{{ site.baseurl }}/assets/image/2401_PUB012535-Nandni_Yadava_2.jpg">
    </div>

    <!-- RIGHT: Long bio -->
    <div class="about-body">

      <p>
        I am a postdoctoral researcher at the <strong>DIII-D National Fusion Facility (General Atomics)</strong> in San Diego, USA. My work focuses on the physics of the tokamak boundary—scrape-off layer and divertor—with an emphasis on <strong>divertor detachment</strong>, Balmer-series spectroscopy, and impurity/neutral dynamics. I apply analysis methods that separate excitation and recombination, quantify particle sources and sinks, and diagnose molecule-assisted processes.
      </p>

      <p>
        I pursued my Bachelor's in 2013 and Master's in 2015 from <a href="https://www.gujaratuniversity.ac.in" target="_blank" rel="noopener">Gujarat University</a>, with Physics as major. 
 
      </p>

      
      <p>
        At DIII-D I collaborate across experiment and modeling teams to design shots, commission and calibrate optical systems, and interpret measurements alongside transport simulations. A recurring theme in my work is turning line-integrated spectra into physics-based, spatially aware inferences that can guide scenario development and control for reliable power exhaust.
      </p>

      <p>
        Before joining DIII-D, I contributed to tokamak research at <strong>ADITYA-U</strong>, where I investigated recycling, impurity influx, and edge temperatures using spectroscopy and imaging. Across projects I enjoy translating complex diagnostics into clear, actionable results for operations and theory groups. My long-term goal is to help bridge diagnostics, modeling, and control so that power-exhaust solutions for future fusion devices are robust and repeatable.
      </p>

      <hr class="hr-soft">

      <p><strong>Research themes:</strong> divertor detachment; edge/SOL transport; Balmer spectroscopy; impurity/neutral dynamics; EIR/MAR; power exhaust; tokamak diagnostics.</p>

      <p><strong>Profiles:</strong>
        <a href="https://orcid.org/0000-0001-5522-2450" target="_blank" rel="noopener">ORCID</a> ·
        <a href="https://scholar.google.com/" target="_blank" rel="noopener">Google Scholar</a> ·
        <a href="https://www.researchgate.net/" target="_blank" rel="noopener">ResearchGate</a> ·
        <a href="https://publons.com/" target="_blank" rel="noopener">Publons</a>
      </p>

    </div>
  </div>
</div>
