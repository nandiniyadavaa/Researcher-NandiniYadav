---
title: About
layout: default
permalink: /
redirect_from:
  - /about
---

<style>
/* Page frame */
.about-wrap{max-width:1100px;margin:0 auto;padding:0 1rem 2rem}
.about-title{ text-align:center;font-size:clamp(1.8rem,2.6vw,2.4rem);font-weight:700;margin:.2rem 0 1.4rem }

/* Intro text with wrapped image */
.about-body{ text-align: justify; hyphens: auto; }
.about-body p{ margin:.75rem 0; line-height:1.7; font-size:1.02rem; color:#222; clear:none !important; }
.about-body a{ color:#0d3ea9; font-weight:600; text-decoration:underline }

/* The photo that text should wrap around */
.about-img{
  float:left !important;
  width:360px;                 /* adjust to taste */
  max-width:40%;
  height:auto;
  margin:0 24px 14px 0;
  border-radius:0 !important;
  box-shadow:none !important;
  shape-outside:inset(0);      /* clean wrap */
}

/* Soft divider */
.hr-soft{ height:1px; background:#e6e6e6; border:0; margin:1.4rem 0 }

/* Clear the float after the intro so later sections start below */
.about-body::after{ content:""; display:block; clear:both; }

/* Keep your original “grid” class available, but neutralize it so it
   doesn’t block text wrapping (you can still use it as a container). */
.about-grid{ display:block; }

/* Mobile: stack image above text, no wrap */
@media (max-width:700px){
  .about-img{ float:none !important; display:block; width:100%; max-width:none; margin:0 0 12px 0; shape-outside:none }
  .about-body{ text-align:left; }
}
</style>

<div class="about-wrap">
  <h1 class="about-title">Dr. Nandini Yadava</h1>

  <!-- INTRO: image + paragraphs in the SAME container so wrap works -->
  <div class="about-body">
    <img class="about-img" src="{{ '/assets/image/2401_PUB012535-Nandni_Yadava_2.jpg' | relative_url }}" alt="Portrait of Dr. Nandini Yadava">

    <p style="text-indent:2em;">
      I am a postdoctoral researcher at the DIII-D National Fusion Facility (General Atomics), San Diego, USA. My work focuses on the physics of the tokamak boundary with an expertise in divertor detachmen, Balmer-series spectroscopy, and impurity/neutral dynamics. I apply Bayesian inference technique to Balmer emissions to separate excitation and recombination, quantify particle sources and sinks, and diagnose molecule-assisted processes.
    </p>

    <p style="text-indent:2em;">
      I contributed to tokamak research at ADITYA-U, where I investigated recycling, impurity influx, and edge temperatures using spectroscopy and Langmuir probe diagnostics. I also, developed MATLAB code to evaluate magnetic-field influenced spectral line shape profile and determining neutral and ion temperatures. My long-term goal is to help bridge diagnostics, modeling, and control so that power-exhaust solutions for future fusion devices are robust and repeatable.
    </p>

    <p style="text-indent:2em;">
      At DIII-D, I collaborate with experimental and modeling teams to design shots, commission and calibrate optical systems, and interpret measurements utilizing transport simulations. A recurring theme in my present work is to link line-integrated spectra to physics-based processes; spatially exploring inferences that can guide future developments leading to control and reliable energy extraction from tokamak devices.
    </p>
    <p><strong>Research themes:</strong> Spectroscopy, divertor detachment, boundary physics, Balmer spectroscopy, impurity/neutral dynamics, power exhaust, tokamak diagnostics.</p>
  </div>

  <hr class="hr-soft">

  <p class="btn-row">
    <a class="btn" href="{{ '/assets/pdfs/N_Yadava_Resume.pdf' | relative_url }}" target="_blank" rel="noopener">Download CV (short)</a>
  </p>
  <p class="btn-row">
    <a class="btn" href="{{ '/assets/pdfs/N_Yadava_CV.pdf' | relative_url }}" target="_blank" rel="noopener">Download CV (full)</a>
  </p>

  <hr class="hr-soft">

  <!-- Keep your sections below; wrapper class retained for your layout hooks -->
  <div class="about-grid">
    <h3>Present activity</h3>
    <p>
      <strong>Postdoctoral researcher</strong> <span class="years">2023–Now</span><br>
      Oak Ridge Associated Universities (ORAU), Tennessee, USA<br>
      DIII-D National Fusion Facility, San Diego, USA
    </p>
    <p style="text-indent:2em;">
      Currently working on quantification of detached plasma to understand power and particle balance. This uses a <strong>Bayesian</strong> inference technique on Balmer emissions and extensive knowledge of atomic &amp; molecular processes, utilizing several existing visible diagnostics of DIII-D. The code is validated for DIII-D with 2024 experimental <strong>measurements</strong> using SAPP (simplest-as-possible plasmas).
    </p>

    <hr class="hr-soft">

    <h3 style="margin-top:1rem">Positions / Experience</h3>
    <p>
      <strong>[2021–2022]</strong> — Senior Research Fellow, Indian Institute of Technology (IIT) Kanpur, Uttar Pradesh<br>
      <strong>[2018–2021]</strong> — Junior Research Fellow, The National Institute of Engineering, Mysuru, Karnataka, India<br>
      <strong>[2016–2018]</strong> — Research Scholar, Gujarat University, Ahmedabad, Gujarat, India<br>
      <strong>[2015–2016]</strong> — Scientific Assistant, Institute for Plasma Research, Gandhinagar, Gujarat, India
    </p>

    <hr class="hr-soft">

    <h3 style="margin-top:1rem">Education</h3>
    <p>
      <strong>[2020–2023]</strong> — Ph.D., Institute of Science, Nirma University, Ahmedabad, Gujarat, India<br>
      <strong>Thesis:</strong>
      <a class="btn" href="{{ '/assets/pdfs/NANDINI YADAV.pdf' | relative_url }}" target="_blank" rel="noopener">
        “Spectroscopic Investigation of Neutrals and Impurity Dynamics in the Edge Region of ADITYA-U Tokamak”
      </a><br>
      <strong>[2013–2015]</strong> — M.Sc., School of Science, Gujarat University, India<br>
      <strong>[2010–2013]</strong> — B.Sc., <em>Bachelor</em> of Science, C. U. Shah Science College, Gujarat University, Ahmedabad, Gujarat, India
    </p>

    <hr class="hr-soft">

    <h3>Achievements</h3>
    <p>
      <strong>[2022]</strong> Buti Young Scientist Award —
      <a class="btn" href="{{ '/assets/pdfs/BUTI_Award.png' | relative_url }}" target="_blank" rel="noopener">certificate</a>,
      <a class="btn" href="{{ '/assets/pdfs/Nandini_Buti_paper_final.pdf' | relative_url }}" target="_blank" rel="noopener">paper</a>,
      <a class="btn" href="{{ '/assets/pdfs/Nandini_Buti_PPT_040222.pdf' | relative_url }}" target="_blank" rel="noopener">ppt</a><br>
      <strong>[2021]</strong> PSSI - Z. H. Sholapurwala Award for Fusion Research<br>
      <strong>[2018]</strong> PSSI visiting student fellowship [Nov 2017 – Mar 2018]<br>
      <strong>[2017]</strong> PSSI poster award<br>
      <strong>[2016]</strong> Selected for the DST-INSPIRE Fellowship<br>
      <strong>[2015]</strong> 1st Rank in M.Sc. Physics at Gujarat University<br>
      <strong>[2013]</strong> 2nd Rank in B.Sc. Physics at Gujarat University
    </p>
  </div>
</div>
