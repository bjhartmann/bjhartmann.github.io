---
layout: frontpage
title: ""
author_profile: true
classes: [hide-title]
hide_meta: true
custom_tab_title: "Björn Hartmann"
---

<style>
/* ===== Page Grid Shell ===== */
#main.frontpage-wide{
  max-width: 1400px;           /* overall page width */
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 240px minmax(0, 1fr);
  column-gap: 2rem;
  align-items: start;
}

/* Sidebar placement */
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

/* Remove theme clamps inside content area */
#main.frontpage-wide .page__inner-wrap,
#main.frontpage-wide .page__content{
  max-width: none !important;
  width: 100% !important;
  min-width: 0 !important;
  float: none !important;
  clear: none !important;
  display: block !important;
}

/* ===== Content Width Control ===== */
/* Center all direct children of content */
.frontpage-wide__content > *{
  max-width: 1400px;     /* wide enough for one-liner */
  width: 100%;
  margin-inline: auto;   /* center horizontally */
}

/* ===== About Block ===== */
.frontpage-wide__content > .about-wrapper{
  box-sizing: border-box;
  display: grid;
  grid-template-columns: 220px 1fr;  /* photo fixed, text flexible */
  column-gap: 1.5rem;
  align-items: start;
  margin: 2rem auto 0;               /* center block */
  max-width: 1400px;
  border: 0 !important;
  background: transparent !important;
  box-shadow: none !important;
  padding: 0;
}

/* About internals */
.about-wrapper img.home-portrait{
  width: 220px;
  height: 220px;
  object-fit: cover;
  border-radius: 50%;
}
.about-text{
  min-width: 0;
  max-width: none !important;  /* text stretches fully */
}

/* ===== Mobile ===== */
@media (max-width: 700px){
  #main.frontpage-wide{ grid-template-columns: 1fr; }
  .about-wrapper{ grid-template-columns: 1fr; }
  .about-wrapper img.home-portrait{ margin-bottom: 1rem; }
}



html, body { height: 100%; }

body{
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  overflow-x: hidden;
}

/* Your main area becomes the flexible spacer */
#main.frontpage-wide{
  flex: 1 0 auto;   /* grow to fill leftover height */
}

/* Footer sits after content without a huge gap */
.page__footer{
  flex-shrink: 0;
  margin-top: 0;    /* keep the gap tight; tweak if you want e.g., 1rem */
}

</style>




<div class="about-wrapper">
  <img src="{{ '/assets/images/me.jpg' | relative_url }}" alt="Björn Hartmann" class="home-portrait" width="220" height="220" loading="eager" decoding="async">
  <div class="about-text">
    <strong>About me</strong>
    <p>I am a 5th year Ph.D. student in Economics at the University of St. Gallen.<br>
    My primary advisor is Reto Föllmi.</p>
    <p>My research interests cover International Trade, Economic Growth, and Structural Change.</p>
    <p>In the academic year 25/26, I visit
    <a href="https://sites.google.com/site/fjbuera/" target="_blank" rel="noopener">Francisco Buera</a> (Washington University in St. Louis) and
    <a href="https://sites.google.com/site/valentinyiakos/" target="_blank" rel="noopener">Ákos Valentinyi</a> (University of Manchester) as a Visiting Researcher.</p>
    <p>You can find my <a href="/files/Academic_CV.pdf" target="_blank" rel="noopener">CV</a>.</p>
  </div>
</div>
