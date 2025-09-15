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



<style id="debug-xray">
/* Outline the main wrappers so we can see their boxes */
.initial-content, .page, .page__layout, .page__inner-wrap,
.page__content, .sidebar {
  outline: 2px dashed rgba(0,0,0,.25);
}

/* Show the element’s computed width in the corner */
.initial-content::after, .page::after, .page__layout::after,
.page__inner-wrap::after, .page__content::after, .sidebar::after {
  content: attr(class) " → " attr(data-mmw);
  position: absolute; font: 12px/1.2 system-ui, sans-serif;
  background: rgba(255,255,0,.85); padding: 2px 6px; border-radius: 4px;
  transform: translateY(-100%); pointer-events: none; color:#000;
}
.initial-content, .page, .page__layout, .page__inner-wrap,
.page__content, .sidebar { position: relative; }

/* Set a CSS var to the computed width via JS below */
</style>
<script>
document.addEventListener('DOMContentLoaded', () => {
  const targets = document.querySelectorAll(
    '.initial-content, .page, .page__layout, .page__inner-wrap, .page__content, .sidebar'
  );
  const update = () => targets.forEach(el => {
    el.setAttribute('data-mmw', Math.round(el.getBoundingClientRect().width)+'px');
  });
  update();
  new ResizeObserver(update).observe(document.documentElement);
});
</script>




<style>
  
/* Uncap every wrapper in the single layout */
.layout--single .initial-content,
.layout--single .page,
.layout--single .page__layout,
.layout--single .page__inner-wrap,
.layout--single .page__content {
  max-width: 1400px !important;
  margin-left: auto !important;
  margin-right: auto !important;
}

/* Let the content column expand next to the sidebar */
.layout--single .page__content {
  max-width: 1100px !important;
  width: auto !important;
  flex: 1 1 auto !important;
}

/* Keep the author sidebar but give it a fixed width */
.layout--single .sidebar {
  flex: 0 0 240px !important;
  max-width: 240px !important;
}

/* Add breathing room at large widths */
.layout--single .page__inner-wrap {
  padding-left: 2rem;
  padding-right: 2rem;
}

/* --- About wrapper layout --- */
.about-wrapper {
  display: grid;
  grid-template-columns: 220px 1fr;   /* photo | text */
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
