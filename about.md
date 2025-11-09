---
layout: default
title: About
permalink: /about/
---

<section class="page-header">
  <div class="wrap">
    <h1>About Me</h1>
    <p class="lead">Power Systems Engineer • M.Eng Student</p>
  </div>
</section>

<section class="about-content">
  <div class="wrap">
    <div class="about-grid">
      <div class="profile-photo">
        <img src="/assets/images/profile.jpg" alt="Sampson Ikechukwu Ewuzie" loading="lazy">
      </div>
      <div class="bio">
        <p>
          I'm <strong>Sampson Ikechukwu Ewuzie</strong>, a <strong>Master of Engineering (M.Eng)</strong> student in Power Systems at [Your University].
        </p>
        <p>
          Passionate about <strong>smart grids, HVDC, renewable integration</strong>, and simulation tools like <strong>MATLAB, PSCAD, ETAP</strong>.
        </p>
        <p>
          This site is my public notebook — tutorials, research, and open-source tools.
        </p>
        <p>
          <a class="btn btn-primary" href="/assets/files/Sampson_Ewuzie_CV_2025.pdf" target="_blank">
            Download CV (PDF)
          </a>
          <a class="btn btn-outline" href="/contact/">Contact Me</a>
        </p>
      </div>
    </div>
  </div>
</section>

<style>
.about-grid { display: grid; gap: 2.5rem; grid-template-columns: 180px 1fr; align-items: start; }
.profile-photo img { width: 100%; border-radius: 50%; border: 4px solid var(--border, #e2e8f0); }
.bio { font-size: 1.1rem; }
@media (max-width: 700px) {
  .about-grid { grid-template-columns: 1fr; text-align: center; }
  .profile-photo img { width: 150px; height: 150px; }
}
</style>