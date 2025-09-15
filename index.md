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
/* — Only affects THIS page because it's inline here — */

/* 1) Uncap the site container */
.layout--single .initial-content {
  max-width: 1400px !important;
  margin-left: auto !important;
  margin-right: auto !important;
}

/* 2) Uncap the article wrapper */
.layout--single .page__inner-wrap {
  max-width: 1400px !important;
}

/* 3) Let the content column actually grow */
.layout--single .page__content {
  max-width: none !important;   /* remove the narrow cap */
  flex: 1 1 auto !important;    /* grow to fill space next to the sidebar */
}

/* Keep the author sidebar but make it a fixed, narrower width */
.layout--single .sidebar {
  flex: 0 0 240px !important;
  max-width: 240px !important;
}
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
