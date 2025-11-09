---
layout: default
title: "Home"
---

<section class="hero">
  <h1>Hello — I'm **Sampson Ikechukwu Ewuzie**</h1>
  <p class="lead">Power Systems Engineer | M.Eng Student | Passionate about Power System Engineering and Smart Grids</p>
  <p>I publish tutorials, research notes, and ideas on power systems, renewable integration, HVDC, power quality and simulation tools like MATLAB, PSCAD and ETAP.</p>

  <p>
    <a class="btn" href="{{ '/blog.html' | relative_url }}">Read the blog</a>
    <a class="btn" href="{{ '/projects.html' | relative_url }}">See projects</a>
  </p>
</section>

<section>
  <h2>Featured post</h2>
  {% assign p = site.posts.first %}
  {% if p %}
    <h3><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>
    <p>{{ p.excerpt | strip_html | truncate: 200 }}</p>
  {% else %}
    <p>No posts yet — start by creating a file in <code>/_posts</code>.</p>
  {% endif %}
</section>
