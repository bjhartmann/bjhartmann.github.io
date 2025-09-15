---
layout: frontpage
title: " "
author_profile: true
classes: [hide-title]
hide_meta: true
custom_tab_title: "Björn Hartmann"
---

<style>
/* Scope only to homepage grid */
#main.frontpage-wide { 
  max-width: 1400px; 
  margin: 0 auto; 
  padding: 0 2rem; 
  display: grid; 
  grid-template-columns: 240px minmax(0, 1fr); 
  column-gap: 2rem; 
  align-items: start;
}

/* Sidebar column */
#main.frontpage-wide .sidebar {
  grid-column: 1;
  grid-row: 1;
  width: 240px;
  max-width: 240px;
}

/* Main article column */
#main.frontpage-wide article.page {
  grid-column: 2;
  grid-row: 1;
}

/* Kill the 770px clamp */
#main.frontpage-wide .page__inner-wrap,
#main.frontpage-wide .page__content {
  max-width: none !important;
  width: 100% !important;
  min-width: 0 !important;
}

/* About section layout */
.about-wrapper {
  display: grid;
  grid-template-columns: 220px 1fr;
  column-gap: 1.5rem;
  align-items: start;
  margin-top: 2rem;
}
.about-wrapper img.home-portrait {
  width: 220px;
  height: 220px;
  object-fit: cover;
  border-radius: 50%;
}
.about-text { min-width: 0; }

/* Stack on mobile */
@media (max-width: 700px) {
  #main.frontpage-wide { grid-template-columns: 1fr; }
  .about-wrapper { grid-template-columns: 1fr; }
  .about-wrapper img.home-portrait { margin-bottom: 1rem; }
}
</style>


<style>
/* Scope to the custom layout only */
#main.frontpage-wide { max-width: 1400px; margin: 0 auto; padding: 0 2rem; }

/* Make the main area a two-column grid: sidebar | content */
#main.frontpage-wide {
  display: grid;
  grid-template-columns: 240px minmax(0, 1fr);
  column-gap: 2rem;
  align-items: start;
}

/* Sidebar column */
#main.frontpage-wide .sidebar {
  grid-column: 1;
  grid-row: 1;
  max-width: 240px;
  width: 240px;
  position: sticky; top: 2rem; /* optional: make it sticky */
}

/* Content column */
#main.frontpage-wide article.page { grid-column: 2; grid-row: 1; }
#main.frontpage-wide .page__content { max-width: none; width: 100%; min-width: 0; }

/* About section inside content: image left, text right */
.about-wrapper { display: grid; grid-template-columns: 220px 1fr; column-gap: 1.5rem; align-items: start; margin-top: 2rem; }
.about-wrapper img.home-portrait { width: 220px; height: 220px; object-fit: cover; border-radius: 50%; }
.about-text { min-width: 0; }

/* Stack on small screens */
@media (max-width: 700px) {
  #main.frontpage-wide { grid-template-columns: 1fr; }
  .about-wrapper { grid-template-columns: 1fr; }
  .about-wrapper img.home-portrait { margin-bottom: 1rem; }
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
