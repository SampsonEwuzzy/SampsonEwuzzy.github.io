---
layout: default
title: "Projects"
---
---
layout: default
title: Projects
permalink: /projects/
---

<!-- Page Header -->
<section class="page-header">
  <div class="wrap">
    <h1>Projects</h1>
    <p class="lead">
      Simulations, research, and open-source tools in power systems, smart grids, and renewable integration.
    </p>
  </div>
</section>

<!-- Projects Grid -->
<section class="projects-grid">
  <div class="wrap">

    <!-- Project 1: Load Flow Simulation -->
    <article class="project-card">
      <div class="project-image">
        <img src="/assets/images/projects/load-flow-screenshot.png" alt="33-bus Load Flow in MATLAB" loading="lazy">
      </div>
      <div class="project-content">
        <h2><a href="https://github.com/SampsonEwuzzy/load-flow-33bus" target="_blank">Load Flow Analysis – 33-Bus System</a></h2>
        <p class="project-meta">MATLAB • PowerWorld • Newton-Raphson</p>
        <p>
          Implemented power flow analysis for a standard IEEE 33-bus distribution network. 
          Solved using Newton-Raphson method with convergence monitoring and voltage profile visualization.
        </p>
        <ul class="project-features">
          <li>Convergence in ≤ 4 iterations</li>
          <li>Interactive voltage & power loss plots</li>
          <li>Exportable CSV results</li>
        </ul>
        <div class="project-links">
          <a href="https://github.com/SampsonEwuzzy/load-flow-33bus" class="btn btn-primary" target="_blank">
            View Code
          </a>
          <a href="https://github.com/SampsonEwuzzy/load-flow-33bus#readme" class="btn btn-outline" target="_blank">
            Read Docs
          </a>
        </div>
      </div>
    </article>

    <!-- Project 2: PV Integration Study -->
    <article class="project-card">
      <div class="project-image">
        <img src="/assets/images/projects/pv-integration.png" alt="Solar PV Integration in PSCAD" loading="lazy">
      </div>
      <div class="project-content">
        <h2><a href="https://github.com/SampsonEwuzzy/pv-grid-integration" target="_blank">Solar PV Grid Integration (PSCAD)</a></h2>
        <p class="project-meta">PSCAD • EMT Simulation • MPPT Control</p>
        <p>
          Modeled a 1 MW solar PV plant with inverter control and grid synchronization. 
          Studied fault ride-through (FRT) and harmonic injection under unbalanced conditions.
        </p>
        <ul class="project-features">
          <li>Real-time EMT simulation</li>
          <li>MPPT & PLL control logic</li>
          <li>IEEE 1547 compliance check</li>
        </ul>
        <div class="project-links">
          <a href="https://github.com/SampsonEwuzzy/pv-grid-integration" class="btn btn-primary" target="_blank">
            View Code
          </a>
          <a href="/blog/2025/11/10/pv-integration-study/" class="btn btn-outline">
            Read Case Study
          </a>
        </div>
      </div>
    </article>

    <!-- Project 3: ETAP Microgrid Design -->
    <article class="project-card">
      <div class="project-image">
        <img src="/assets/images/projects/microgrid-etap.png" alt="Microgrid Design in ETAP" loading="lazy">
      </div>
      <div class="project-content">
        <h2><a href="https://github.com/SampsonEwuzzy/microgrid-etap" target="_blank">Islanded Microgrid Design</a></h2>
        <p class="project-meta">ETAP • Load Sharing • Droop Control</p>
        <p>
          Designed a hybrid microgrid with diesel, solar, and battery storage. 
          Implemented frequency and voltage droop control for seamless islanding.
        </p>
        <ul class="project-features">
          <li>Dynamic load sharing</li>
          <li>Black start capability</li>
          <li>Protection coordination</li>
        </ul>
        <div class="project-links">
          <a href="https://github.com/SampsonEwuzzy/microgrid-etap" class="btn btn-primary" target="_blank">
            View Model
          </a>
          <a href="#" class="btn btn-outline disabled" title="Coming soon">
            View Report
          </a>
        </div>
      </div>
    </article>

    <!-- Add more projects above this line -->

    <!-- "More Coming Soon" Placeholder -->
    <div class="project-card coming-soon">
      <div class="project-content">
        <h2>More Projects Coming Soon...</h2>
        <p>HVDC Simulation • Fault Analysis • Python Automation Tools</p>
      </div>
    </div>

  </div>
</section>

<!-- Inline Styles (will inherit from style.css + add project-specific) -->
<style>
.projects-grid {
  padding: 4rem 0;
  background: #fafafa;
}
.project-card {
  background: #fff;
  border: 1px solid var(--border);
  border-radius: var(--radius);
  overflow: hidden;
  margin-bottom: 2rem;
  display: flex;
  flex-direction: row;
  transition: var(--transition);
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
}
.project-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 20px rgba(0,0,0,0.1);
}
.project-image {
  flex: 0 0 280px;
  overflow: hidden;
}
.project-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.4s ease;
}
.project-card:hover .project-image img {
  transform: scale(1.05);
}
.project-content {
  padding: 1.5rem;
  flex: 1;
  display: flex;
  flex-direction: column;
}
.project-content h2 {
  margin: 0 0 0.5rem;
  font-size: 1.4rem;
}
.project-content h2 a {
  color: var(--text);
  text-decoration: none;
}
.project-content h2 a:hover {
  color: var(--accent);
}
.project-meta {
  font-size: 0.9rem;
  color: var(--accent-dark);
  font-weight: 600;
  margin-bottom: 0.75rem;
}
.project-features {
  list-style: none;
  padding: 0;
  margin: 1rem 0;
  font-size: 0.95rem;
  color: var(--muted);
}
.project-features li {
  position: relative;
  padding-left: 1.4rem;
  margin: 0.35rem 0;
}
.project-features li::before {
  content: "✓";
  color: var(--accent);
  position: absolute;
  left: 0;
  font-weight: bold;
}
.project-links {
  margin-top: auto;
  display: flex;
  gap: 0.75rem;
  flex-wrap: wrap;
}
.project-links .btn {
  font-size: 0.9rem;
  padding: 0.5rem 1rem;
}
.coming-soon {
  background: linear-gradient(135deg, #f0f7ff, #e6f0ff);
  border: 2px dashed var(--accent);
  text-align: center;
  justify-content: center;
}
.coming-soon h2 {
  color: var(--accent-dark);
  font-size: 1.3rem;
}
.disabled {
  opacity: 0.5;
  cursor: not-allowed;
}

/* Responsive */
@media (max-width: 800px) {
  .project-card {
    flex-direction: column;
  }
  .project-image {
    flex: none;
    height: 180px;
  }
}
</style>
