---
layout: single
title: ""               
author_profile: false
classes: [hide-title]
permalink: /
---


<style>
/* Profile row: photo + short info */
.profile-row {
  display: grid;
  grid-template-columns: 220px 1fr;
  column-gap: 4rem;
  align-items: center;
  max-width: 900px;
  margin: 0 auto 1.5rem;
}
.profile-row img.home-portrait {
  width: 220px;
  height: 220px;
  object-fit: cover;
  border-radius: 50%;
}

/* About text block below the profile row */
.about-text {
  max-width: 900px;
  margin: 0 auto;
  line-height: 1.6;
}

/* Mobile adjustments */
@media (max-width: 720px){
  .profile-row {
    grid-template-columns: 1fr;
    row-gap: 1rem;
  }
  .profile-row img.home-portrait {
    margin: 0 auto;
  }
}

.profile-meta a {
  color: inherit;          /* take surrounding text color */
  text-decoration: none;   /* remove underline */
}
.profile-meta a:hover {
  text-decoration: underline; /* optional subtle hover effect */
}


</style>


<div class="profile-row">
  <img src="{{ '/assets/images/me.jpg' | relative_url }}" alt="Björn Hartmann" class="home-portrait" width="220" height="220" loading="eager" decoding="async">
  <div class="profile-meta">
    <p><strong>Björn Hartmann</strong></p>
    <p>
      <i class="fa fa-envelope"></i>
      <a href="mailto:YOUR_EMAIL@DOMAIN">Email</a>
    </p>
    <p>
      <i class="fa fa-file-alt"></i>
      <a href="/files/Academic_CV.pdf" target="_blank" rel="noopener">CV</a>
    </p>
    <p>
      <i class="fa fa-university"></i>
      <a href="https://www.unisg.ch/en/" target="_blank" rel="noopener">University of St. Gallen</a>
    </p>
  </div>
</div>



<section class="about-text">
  <strong>About me</strong>
  <p>I am a 5th year Ph.D. student in Economics at the University of St. Gallen.<br> My primary advisor is Reto Föllmi.</p>
  <p>My research interests cover International Trade, Economic Growth, and Structural Change.</p>
  <p>In the academic year 25/26, I visit
    <a href="https://sites.google.com/site/fjbuera/" target="_blank" rel="noopener">Francisco Buera</a> (Washington University in St. Louis) and<br>
    <a href="https://sites.google.com/site/valentinyiakos/" target="_blank" rel="noopener">Ákos Valentinyi</a> (University of Manchester) as a Visiting Researcher.</p>
</section>

