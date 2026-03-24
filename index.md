---
layout: single
title: ""               
author_profile: false
classes: [hide-title]
permalink: /
---

<style>
/* Top row: text left, photo right */
.profile-row {
  display: grid;
  grid-template-columns: 1fr 260px;
  column-gap: 4rem;
  align-items: center;
  max-width: 900px;
  margin: 0 auto 1.5rem;
}

/* Portrait image: keep original aspect ratio */
.profile-row img.home-portrait {
  width: 260px;
  height: auto;
  display: block;
  object-fit: contain;
  border-radius: 12px; /* use 0 if you want sharp corners */
  justify-self: end;
}

/* Text block */
.about-text {
  max-width: 900px;
  margin: 0 auto;
  line-height: 1.6;
}

.profile-meta {
  margin-top: 1.5rem;
  display: flex;
  gap: 3rem;
  align-items: center;
  flex-wrap: wrap;
}

.profile-meta p {
  margin: 0;
}

.profile-meta a {
  color: inherit;
  text-decoration: none;
}

.profile-meta a:hover {
  text-decoration: underline;
}

/* Mobile */
@media (max-width: 720px){
  .profile-row {
    grid-template-columns: 1fr;
    row-gap: 1rem;
  }

  .profile-row img.home-portrait {
    justify-self: center;
    width: 220px;
  }
}
</style>

<div class="profile-row">
  <section class="about-text">
    <strong>About me</strong>
    <p>I am a 5th year Ph.D. student in Economics at the University of St. Gallen.<br> My primary advisor is Reto Föllmi.</p>
    <p>My research interests cover International Trade, Economic Growth, and Structural Change.</p>
    <p>In the academic year 25/26, I visit
      <a href="https://sites.google.com/site/fjbuera/" target="_blank" rel="noopener">Francisco Buera</a> (Washington University in St. Louis) and<br>
      <a href="https://sites.google.com/site/valentinyiakos/" target="_blank" rel="noopener">Ákos Valentinyi</a> (University of Manchester) as a Visiting Researcher.</p>

    <div class="profile-meta">
      <p>
        <i class="fa fa-envelope fa-fw"></i>
        <a href="mailto:bjoern.hartmann@unisg.ch">Email</a>
      </p>
      <p>
        <i class="fa fa-file-alt fa-fw"></i>
        <a href="/files/Academic_CV.pdf" target="_blank" rel="noopener">CV</a>
      </p>
    </div>
  </section>

  <img src="{{ '/assets/images/Björn_5.jpg' | relative_url }}" alt="Björn Hartmann" class="home-portrait" loading="eager" decoding="async">
</div>
