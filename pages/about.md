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
      <p style="text-indent:2em;">
        I am a postdoctoral researcher at the <strong>DIII-D National Fusion Facility (General Atomics), San Diego, USA</strong>. My work focuses on the physics of the tokamak boundary—scrape-off layer and divertor—with an experties on <strong>divertor detachment</strong>, Balmer-series spectroscopy, and impurity/neutral dynamics. I apply analysis methods that separate excitation and recombination, quantify particle sources and sinks, and diagnose molecule-assisted processes.
      </p>

      <p style="text-indent:2em;">
        I contributed to tokamak research at ADITYA-U, where I investigated recycling, impurity influx, and edge temperatures using spectroscopy and imaging. Across projects I enjoy translating complex diagnostics into clear, actionable results for operations and theory groups. My long-term goal is to help bridge diagnostics, modeling, and control so that power-exhaust solutions for future fusion devices are robust and repeatable.
      </p>
      
      <p style="text-indent:2em;">
        At DIII-D, I collaborate with experimental and modeling teams to design shots, commission and calibrate optical systems, and interpret measurements utilizing transport simulations. A recurring theme in my present work is to link line-integrated spectra to physics-based processes; spatially exploring inferences that can guide future  developments leading to   control and  reliable energy extraction from tokamak.
      </p>


      <hr class="hr-soft">
      <p><strong>Research themes:</strong> divertor detachment; edge/SOL transport; Balmer spectroscopy; impurity/neutral dynamics; EIR/MAR; power exhaust; tokamak diagnostics.</p>
    <hr class="hr-soft">
    <p class="btn-row">
        <a class="btn" href="{{ '/assets/pdfs/N_Yadava_Resume.pdf' | relative_url }}" target="_blank" rel="noopener">Download CV (short)            </a>
    </p>
    <p class="btn-row">
        <a class="btn" href="{{ '/assets/pdfs/N_Yadava_CV.pdf' | relative_url }}" target="_blank" rel="noopener">Download CV (full) </a>
    </p>
    <hr class="hr-soft">
      <h3>Present activity</h3>
      <p>
        <strong>Postdoctoral researcher</strong> <span class="years">2023–Now</span><br>
        Oak Ridge Associated University, Tennessee, USA<br>
        DIII-D National Fusion Facility, San Diego, USA<br>
        <p style="text-indent:2em;">
          Currently working on quantification of the detached plasma to understand power and particle balance. This requires use of Bayseian inference technique on Balmer emissions. Also, it needs extensive understanding of atomic & molecular processes. This utilizes several existing visible diagnostics of DIII-D. The code is validated for DIII-D with 2024 experimental mesurements using SAPP (simplest as possible plasmas).
        </p>
     
      <hr class="hr-soft">
      
      <h3 style="margin-top:1rem">Positions / Experience</h3>
      <p>
        <strong>[2021–2022]</strong> <span class="years"></span> — Senior Research Fellow, Indian Institute of Technology (IIT) Kanpur, Uttar Pradesh<br>
        <strong>[2018–2021]</strong> <span class="years"></span> — Junior Research Fellow, The National Institute of Engineering, Mysuru, Karnataka, India<br>
        <strong>[2016–2018]</strong> <span class="years"></span> — Research Scholar, Gujarat University, Ahmedabad, Gujarat, India<br>
        <strong>[2015–2016]</strong> <span class="years"></span> — Scientific Assistant, Institute for Plasma Research, Gandhinagar, Gujarat, India<br>
      </p>
      <hr class="hr-soft">
      <h3 style="margin-top:1rem">Education</h3>
      <p>
        <strong>[2020–2023]</strong> <span class="years"></span> — Ph.D., Institute of Science, Nirma University, Ahmedabad, Gujarat, India<br>
        <strong>Thesis:</strong><a class="btn" href="{{ '/assets/pdfs/NANDINI YADAV.pdf' | relative_url }}" target="_blank" rel="noopener">“Spectroscopic Investigation of Neutrals and Impurity Dynamics in the Edge Region of ADITYA-U Tokamak”   </a><br>
        <strong>[2013–2015]</strong> <span class="years"></span> — M.Sc., Master of Science, School of Science, Gujarat University, India<br>
        <strong>[2010–2013]</strong> <span class="years"></span> — B.Sc., Bachlor of Science, C. U. Shah Science College, Gujarat University, Ahmedabad, Gujarat, India<br>
      </p>
      <hr class="hr-soft">
      
      <h3>Achievements</h3>
      <p>
      <strong>[2022]</strong> Buti Young Scientist Award      
        <a class="btn" href="{{ '/assets/pdfs/BUTI_Award.png' | relative_url }}" target="_blank" rel="noopener"> certificate, </a>
        <a class="btn" href="{{ '/assets/pdfs/Nandini_Buti_paper_final.pdf' | relative_url }}" target="_blank" rel="noopener"> paper, </a>
        <a class="btn" href="{{ '/assets/pdfs/Nandini_Buti_PPT_040222.pdf' | relative_url }}" target="_blank" rel="noopener"> ppt </a>
      <br> 
      <strong>[2021]</strong> PSSI - Z. H. Sholapurwala Award for Fusion Research<br>
      <strong>[2018]</strong> PSSI visiting student fellowship [November 2017 to March 2018]<br>
      <strong>[2017]</strong> PSSI poster award <br>
      <strong>[2016]</strong> Selected for the DST-INSPIRE Fellowship <br>
      <strong>[2015]</strong> 1st Rank in M.Sc. Physics at Gujarat University <br>
      <strong>[2013]</strong> 2nd Rank in M.Sc. Physics at Gujarat University <br>
      </p>
    </div>
    </div>
    </div>
