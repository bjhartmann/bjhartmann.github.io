---
layout: frontpage
title: " "
author_profile: true
classes: [hide-title]
hide_meta: true
custom_tab_title: "Björn Hartmann"
---

<style>

 /* Debug (optional) */
#main.frontpage-wide { outline: 3px solid red; }
#main.frontpage-wide .sidebar { outline: 3px dashed blue; }
#main.frontpage-wide article.page { outline: 3px dashed green; }
#main.frontpage-wide .page__inner-wrap { outline: 2px dotted orange; }
#main.frontpage-wide .page__content { outline: 2px dotted purple; }
.about-wrapper { outline: 2px solid teal; }
.about-wrapper img.home-portrait { outline: 2px solid pink; }
.about-text { outline: 2px solid brown; }

/* Outer wrapper */
.initial-content {
  max-width: 1600px !important;
  margin: 0 auto;                 /* center the whole page */
  padding: 0 2rem;
}

/* Frontpage grid: sidebar | content */
#main.frontpage-wide{
  max-width: 1600px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 240px minmax(0, 1fr);
  column-gap: 2rem;
  align-items: start;
}

/* Sidebar */
#main.frontpage-wide .sidebar{
  grid-column: 1;
  grid-row: 1;
  width: 240px;
  max-width: 240px;
  position: sticky;
  top: 2rem;
}

/* Content column */
#main.frontpage-wide article.page{
  grid-column: 2;
  grid-row: 1;
  min-width: 0; /* prevent overflow in grid */
}

/* Remove the theme’s clamp/float here only */
#main.frontpage-wide .page__inner-wrap,
#main.frontpage-wide .page__content{
  max-width: none !important;
  width: 100% !important;
  min-width: 0 !important;
  float: none !important;
  clear: none !important;
  display: block !important;
}

/* Default reading width for all direct children of page__content */
#main.frontpage-wide article.page .page__content > * {
  max-width: 980px;
  width: 100%;
  margin-inline: auto;  /* centered */
}

/* Teal box ONLY: wider and centered */
.about-wrapper{
  max-width: 1200px;            /* ← adjust to taste: 1100–1200 */
  margin-inline: auto;
  display: grid;
  grid-template-columns: 220px 1fr;
  column-gap: 1.5rem;
  align-items: start;
  margin-top: 2rem;
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
