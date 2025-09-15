---
layout: frontpage
title: " "
author_profile: true
classes: [hide-title]
hide_meta: true
custom_tab_title: "Björn Hartmann"
---

<style>

  /* Debug: visualize layout boxes */
#main.frontpage-wide {
  outline: 3px solid red;      /* outer grid */
}

#main.frontpage-wide .sidebar {
  outline: 3px dashed blue;    /* sidebar */
}

#main.frontpage-wide article.page {
  outline: 3px dashed green;   /* content column */
}

#main.frontpage-wide .page__inner-wrap {
  outline: 2px dotted orange;  /* inner wrapper */
}

#main.frontpage-wide .page__content {
  outline: 2px dotted purple;  /* actual content */
}

.about-wrapper {
  outline: 2px solid teal;     /* about block wrapper */
}

.about-wrapper img.home-portrait {
  outline: 2px solid pink;     /* portrait image */
}

.about-text {
  outline: 2px solid brown;    /* text box */
}


  
/* Outer site wrapper — let the page breathe */
.initial-content {
  max-width: 1600px !important;   /* ↑ was 1400; this was the choke point */
  margin-left: 0; 
  margin-right: auto;
  padding-left: 2rem;
  padding-right: 2rem;
}

/* Scope ONLY to this page via #main.frontpage-wide */
#main.frontpage-wide{
  max-width: 1600px;
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

.about-wrapper {
  max-width: 1200px;   /* wider than the 980px text column */
  margin-left: auto;   /* keep it centered */
  margin-right: auto;
  display: grid;
  grid-template-columns: 220px 1fr;
  column-gap: 1.5rem;
  align-items: start;
  margin-top: 2rem;
}


/* Content column */
#main.frontpage-wide article.page{
  max-width: 1600px;
  grid-column: 2;
  grid-row: 1;
  min-width: 0;                 /* critical for grid overflow */
}


/* Remove the theme's clamp + float layout ONLY here */
#main.frontpage-wide .page__inner-wrap,
#main.frontpage-wide .page__content{
  max-width: none !important;
  width: 100% !important;
  min-width: 0 !important;
  float: none !important;
  clear: none !important;
  display: block !important;
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

  /* UNCAP the container so the teal box can exceed 980 */
#main.frontpage-wide article.page .page__content {
  max-width: none !important;
}

/* Keep 980px reading width for everything EXCEPT the teal .about-wrapper */
#main.frontpage-wide article.page .page__content > :not(.about-wrapper) {
  max-width: 980px;
  width: 100%;
  margin-inline: auto;
}

/* Teal box: make it a bit wider and centered */
.about-wrapper {
  max-width: 1100px;          /* adjust: 1050–1200 to taste */
  margin-inline: auto;
  display: grid;
  grid-template-columns: 220px 1fr;
  column-gap: 1.5rem;
  align-items: start;
  margin-top: 2rem;
}

  
/* Stack on mobile */
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
