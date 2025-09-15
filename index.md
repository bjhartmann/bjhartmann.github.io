---
layout: frontpage
title: " "
author_profile: true
classes: [hide-title]
hide_meta: true
custom_tab_title: "Björn Hartmann"
---

<style>
/* Scope ONLY to this page via #main.frontpage-wide */
#main.frontpage-wide{
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;

  /* Sidebar | Content grid */
  display: grid;
  grid-template-columns: 240px minmax(0, 1fr);
  column-gap: 2rem;
  align-items: start;
}

/* Sidebar column */
#main.frontpage-wide .sidebar{
  grid-column: 1;
  grid-row: 1;
  width: 240px;
  max-width: 240px;
  position: sticky;      /* optional */
  top: 2rem;
}

/* Content column */
#main.frontpage-wide article.page{
  grid-column: 2;
  grid-row: 1;
}

/* Remove the theme's 770px clamp ONLY here */
#main.frontpage-wide .page__inner-wrap,
#main.frontpage-wide .page__content{
  max-width: none !important;
  width: 100% !important;
  min-width: 0 !important;
  flex: 1 1 auto !important;    /* neutralize flex sizing */
}

/* About block: image left, text right */
.about-wrapper{
  display: grid;
  grid-template-columns: 220px 1fr;
  column-gap: 1.5rem;
  align-items: start;
  margin-top: 2rem;
}
.about-wrapper img.home-portrait{
  width: 220px; height: 220px; object-fit: cover; border-radius: 50%;
}
.about-text{ min-width: 0; }

/* Stack on mobile */
@media (max-width: 700px){
  #main.frontpage-wide{ grid-template-columns: 1fr; }
  .about-wrapper{ grid-template-columns: 1fr; }
  .about-wrapper img.home-portrait{ margin-bottom: 1rem; }
}
</style>

<style>
/* FRONT PAGE ONLY — kill float-based layout so grid can stretch the column */
#main.frontpage-wide .page__inner-wrap,
#main.frontpage-wide .page__content {
  float: none !important;
  display: block !important;
  width: 100% !important;      /* keep full column width */
  max-width: none !important;  /* you've already set this */
  min-width: 0 !important;     /* allow shrinking without wrapping */
  clear: none !important;      /* theme sets clear: both; unset it */
}

/* Make sure the grid track can actually grow */
#main.frontpage-wide article.page {
  min-width: 0;                /* critical for grid/flex overflow */
}
#main.frontpage-wide .page__inner-wrap {
  min-width: 0;
  box-sizing: border-box;
}

/* (Optional) widen the outer site wrapper a bit */
.initial-content {             /* this wrapper sits outside #main */
  max-width: 1400px !important;
  margin-left: auto;
  margin-right: auto;
  padding-left: 2rem;
  padding-right: 2rem;
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
