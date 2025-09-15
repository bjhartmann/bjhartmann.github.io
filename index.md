---
layout: single
title: " "
author_profile: true
classes: [hide-title]
hide_meta: true
custom_tab_title: "Björn Hartmann"
redirect_from:
  - /about/
  - /about.html
---

<!-- Give THIS page a unique body class so overrides apply only here -->
<script>
  document.addEventListener('DOMContentLoaded', () => {
    document.body.classList.add('about-override');
  });
</script>

<style>
/* — Only affects THIS page because it's scoped to .about-override — */

/* Let the overall single-page wrapper breathe */
body.about-override.layout--single .initial-content,
body.about-override.layout--single .page,
body.about-override.layout--single .page__layout,
body.about-override.layout--single .page__inner-wrap {
  max-width: 1400px !important;
  margin-left: auto !important;
  margin-right: auto !important;
  padding-left: 2rem;
  padding-right: 2rem;
}

/* Keep the author sidebar but fix a sensible width */
body.about-override.layout--single .sidebar {
  flex: 0 0 240px !important;
  max-width: 240px !important;
}

/* Beat the theme’s 770px clamp for the main content column */
body.about-override.layout--single article.page .page__content {
  max-width: 1100px !important;   /* tweak to taste */
  width: auto !important;
  flex: 1 1 auto !important;
}

/* --- About section (Grid): photo left, text right --- */
.about-wrapper {
  display: grid;
  grid-template-columns: 220px 1fr;  /* image | text */
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

/* Stack only on small screens */
@media (max-width: 700px) {
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
