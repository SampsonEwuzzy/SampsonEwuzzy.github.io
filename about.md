---
layout: default
title: About
permalink: /about/
---

<section class="page-header">
  <div class="wrap">
    <h1>About Me</h1>
    <p class="lead">
      Power Systems Engineer • M.Eng Candidate • Passionate about sustainable grids.
    </p>
  </div>
</section>

<section class="about-content">
  <div class="wrap">
    <div class="about-grid">
      <!-- Profile Photo -->
      <div class="profile-photo">
        <img src="/assets/images/profile.jpg" alt="Sampson Ikechukwu Ewuzie" loading="lazy">
      </div>

      <!-- Bio -->
      <div class="bio">
        <h2>Hello, I'm Sampson</h2>
        <p>
          I’m currently pursuing a <strong>Master of Engineering in Power Systems</strong> at
          <em>[Your University]</em>. My research focuses on <strong>renewable energy integration,
          HVDC transmission, and smart grid technologies</strong>.
        </p>
        <p>
          With hands-on experience in <strong>MATLAB/Simulink, PSCAD, ETAP, and DIgSILENT</strong>,
          I enjoy translating complex theory into practical simulations and tutorials.
        </p>
        <p>
          This site is my public notebook — a place to share class insights, simulation workflows,
          and ideas for the future of energy.
        </p>

        <h3>Skills & Tools</h3>
        <ul class="skills">
          <li>Power Flow & Fault Analysis</li>
          <li>Renewable Integration Modeling</li>
          <li>HVDC & FACTS Devices</li>
          <li>Python, MATLAB, PSCAD, ETAP</li>
          <li>LaTeX, Markdown, Jekyll</li>
        </ul>

        <p>
          <a class="btn btn-primary" href="/assets/files/Sampson_Ewuzie_Resume.pdf" target="_blank">
            Download CV (PDF)
          </a>
          <a class="btn btn-outline" href="/contact/">Contact Me</a>
        </p>
      </div>
    </div>
  </div>
</section>

<style>
.about-grid {
  display: grid;
  gap: 2.5rem;
  grid-template-columns: 200px 1fr;
  align-items: start;
}
.profile-photo img {
  width: 100%;
  border-radius: 50%;
  border: 4px solid var(--border);
}
.bio h2 { margin-top: 0; }
.skills {
  columns: 2;
  list-style: none;
  padding: 0;
}
.skills li {
  margin: .4rem 0;
  position: relative;
  padding-left: 1.2rem;
}
.skills li::before {
  content: "✓";
  color: var(--accent);
  position: absolute;
  left: 0;
}
@media (max-width: 700px) {
  .about-grid { grid-template-columns: 1fr; text-align: center; }
  .profile-photo img { width: 160px; height: 160px; }
  .skills { columns: 1; }
}
</style>