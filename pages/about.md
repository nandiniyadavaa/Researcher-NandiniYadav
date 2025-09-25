---
title: About
layout: default
permalink: /
redirect_from:
  - /about
---


<style>
/* About page layout */
.about-wrap{max-width:1100px;margin:0 auto;padding:0 1rem 2rem}
.about-title{ text-align:center;font-size:clamp(1.8rem,2.6vw,2.4rem);font-weight:700;margin:.2rem 0 1.4rem }

/* WRAP AROUND PHOTO + SQUARE EDGES */
.about-body{ text-align: justify; hyphens: auto; }
.about-photo img{
  float: left;                  /* wrap text around the image */
  width: 360px;                 /* size of photo; adjust to taste */
  max-width: 40%;
  height: auto;
  margin: 0 24px 14px 0;
  border-radius: 0 !important;  /* override any global “circle image” rule */
  box-shadow: none !important;  /* remove soft frame/shadow if you don’t want it */
  shape-outside: inset(0);      /* keep wrap clean */
}

/* clear the float after the text block */
.about-body::after{ content:""; display:block; clear:both; }

/* paragraph/link styling */
.about-body p{ margin:.75rem 0; line-height:1.7; font-size:1.02rem; color:#222 }
.about-body a{ color:#0d3ea9; font-weight:600; text-decoration:underline }
.hr-soft{ height:1px; background:#e6e6e6; border:0; margin:1.4rem 0 }

/* mobile: stack image above text, no wrap */
@media (max-width:700px){
  .about-photo img{ float:none; display:block; width:100%; max-width:none; margin:0 0 12px 0; shape-outside:none }
  .about-body{ text-align:left; }
}

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
