---
layout: default
title: Home
---

<section class="hero">
  <div class="wrap">
    <h1>Hello — I'm <strong>Sampson Ikechukwu Ewuzie</strong></h1>
    <p class="lead">Power Systems Engineer • M.Eng Student</p>
    <p>I share tutorials, simulations, and insights on smart grids, HVDC, and renewable integration.</p>
    <p>
      <a class="btn btn-primary" href="/blog/">Read Blog</a>
      <a class="btn btn-outline" href="/projects/">View Projects</a>
    </p>
  </div>
</section>

<section class="featured">
  <div class="wrap">
    <h2>Latest Post</h2>
    {% assign post = site.posts.first %}
    {% if post %}
      <div class="post-card">
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
        <p>{{ post.excerpt | strip_html | truncate: 240 }}</p>
        <a class="read-more" href="{{ post.url }}">Read more</a>
      </div>
    {% endif %}
  </div>
</section>