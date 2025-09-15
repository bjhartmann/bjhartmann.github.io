---
layout: single
title: " "
author_profile: true
classes: [slim, hide-title]
hide_meta: true
custom_tab_title: "Björn Hartmann"
redirect_from:
  - /about/
  - /about.html
---


<style>
/* --- About layout --- */
.about-wrapper {
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
  margin-top: 2rem;
}
.about-wrapper img.home-portrait {
  width: 220px;
  height: 220px;
  object-fit: cover;
  border-radius: 50%;
}
.about-text { flex: 1; }

@media (max-width: 768px) {
  .about-wrapper { display: block; }
  .about-wrapper img.home-portrait { margin-bottom: 1rem; }
}

/* --- Widen content ONLY on this page (body has `slim`) --- */
/* Minimal Mistakes caps width on several wrappers; raise all of them. */
.slim .initial-content,
.slim .page,
.slim .page__inner,
.slim .page__content {
  max-width: 1350px !important;   /* slightly wider than the ~1200px default */
  margin-left: auto;
  margin-right: auto;
}

/* If this still doesn't move, uncomment the line below to confirm selectors hit:
.slim .initial-content, .slim .page, .slim .page__inner, .slim .page__content { max-width: none !important; }
*/
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
