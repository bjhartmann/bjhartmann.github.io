---
layout: single
title: " "
author_profile: true
classes: [wide, hide-title]
hide_meta: true
custom_tab_title: "Björn Hartmann"
redirect_from:
  - /about/
  - /about.html
---


<style>
/* — Only this page — */

/* Uncap EVERY wrapper used by the single layout */
.layout--single .initial-content,
.layout--single .page,               /* some versions add this */
.layout--single .page__layout,       /* and/or this */
.layout--single .page__inner-wrap,
.layout--single .page__content {
  max-width: 1400px !important;
  margin-left: auto !important;
  margin-right: auto !important;
}

/* Let the content column actually expand next to the sidebar */
.layout--single .page__content {
  max-width: none !important;
  width: auto !important;
  flex: 1 1 auto !important;
}

/* Keep the author sidebar but give it a fixed, narrower width */
.layout--single .sidebar {
  flex: 0 0 240px !important;
  max-width: 240px !important;
}

/* (Optional) a bit more breathing room at large widths */
.layout--single .page__inner-wrap { padding-left: 2rem; padding-right: 2rem; }
</style>



<div class="about-wrapper">
  <img src="{{ '/assets/images/me.jpg' | relative_url }}" alt="Björn Hartmann" class="home-portrait">
  
  <div class="about-text">
    <strong>About me</strong>
    <p>I am a 5th year Ph.D. student in Economics at the University of St. Gallen. 
    My primary advisor is Reto Föllmi.</p>
    <p>My research interests cover International Trade, Economic Growth, and Structural Change.</p>
    <p>In the academic year 25/26, I visit
    <a href="https://sites.google.com/site/fjbuera/" target="_blank" rel="noopener">Francisco Buera</a> (Washington University in St. Louis) and 
    <a href="https://sites.google.com/site/valentinyiakos/" target="_blank" rel="noopener">Ákos Valentinyi</a> (University of Manchester) as a Visiting Researcher.</p>
    <p>You can find my CV <a href="/files/Academic_CV.pdf" target="_blank" rel="noopener">here</a>.</p>
  </div>
</div>
