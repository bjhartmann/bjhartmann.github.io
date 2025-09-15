---
layout: frontpage
title: ""
author_profile: true
classes: [hide-title]
hide_meta: true
custom_tab_title: "Björn Hartmann"
---

<style>
/* Grid shell for front page */
#main.frontpage-wide{
  max-width: 1600px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 240px minmax(0, 1fr);
  column-gap: 2rem;
  align-items: start;
}

/* Sidebar and content placement */
#main.frontpage-wide .sidebar{
  grid-column: 1;
  grid-row: 1;
  width: 240px;
  position: sticky;
  top: 2rem;
}
#main.frontpage-wide article.page{
  grid-column: 2;
  grid-row: 1;
  min-width: 0;
}

/* Remove theme clamps for this page’s content area */
#main.frontpage-wide .page__inner-wrap,
#main.frontpage-wide .page__content{
  max-width: none !important;
  width: 100% !important;
  min-width: 0 !important;
  float: none !important;
  clear: none !important;
  display: block !important;
}

/* Default reading width for everything in this page’s content */
.frontpage-wide__content > *{
  max-width: 980px;
  width: 100%;
  margin-inline: auto;
}

/* Teal "About" box: left-locked, expands right, stops before edge */
.frontpage-wide__content > .about-wrapper{
  box-sizing: border-box;
  width: 100%;
  margin-left: 0;            /* stay under the portrait/left edge */
  margin-right: auto;        /* expand to the right */
  max-width: min(1400px, calc(100% - 3rem)); /* ~3rem gap to column edge */
  display: grid;
  grid-template-columns: 220px 1fr;
  column-gap: 1.5rem;
  align-items: start;
  margin-top: 2rem;
  border: 1px solid #1d9aa5;           /* optional styling */
  border-radius: 6px;
  padding: 1rem;
  background: #f6fbfc;
}

/* About internals */
.about-wrapper img.home-portrait{
  width: 220px; height: 220px; object-fit: cover; border-radius: 50%;
}
.about-text{ min-width: 0; }

/* Mobile stack */
@media (max-width: 700px){
  #main.frontpage-wide{ grid-template-columns: 1fr; }
  .about-wrapper{ grid-template-columns: 1fr; }
  .about-wrapper img.home-portrait{ margin-bottom: 1rem; }
}
</style>

<div class="about-wrapper">
  <img src="{{ '/assets/images/me.jpg' | relative_url }}" alt="Björn Hartmann" class="home-portrait" width="220" height="220" loading="eager" decoding="async">
  <div class="about-text">
    <strong>About me</strong>
    <p>I am a 5th year Ph.D. student in Economics at the University of St. Gallen.
    My primary advisor is Reto Föllmi.</p>
    <p>My research interests cover International Trade, Economic Growth, and Structural Change.</p>
    <p>In the academic year 25/26, I visit
    <a href="https://sites.google.com/site/fjbuera/" target="_blank" rel="noopener">Francisco Buera</a> (Washington University in St. Louis) and
    <a href="https://sites.google.com/site/valentinyiakos/" target="_blank" rel="noopener">Ákos Valentinyi</a> (University of Manchester) as a Visiting Researcher.</p>
    <p>You can find my <a href="/files/Academic_CV.pdf" target="_blank" rel="noopener">CV (PDF)</a>.</p>
  </div>
</div>
