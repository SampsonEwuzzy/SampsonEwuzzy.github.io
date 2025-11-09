---
layout: default
title: Home
---

<!-- HERO SECTION -->
<section class="hero">
  <div class="hero-content">
    <h1>Hello — I'm <strong>Sampson Ikechukwu Ewuzie</strong></h1>
    <p class="lead">
      Power Systems Engineer • M.Eng Student • Smart Grids & Renewable Integration
    </p>
    <p class="intro">
      I share tutorials, research notes, and ideas on power systems, HVDC, power quality,
      and simulation tools like MATLAB, PSCAD & ETAP.
    </p>

    <div class="hero-actions">
      <a class="btn btn-primary" href="{{ '/blog.html' | relative_url }}">Read the Blog</a>
      <a class="btn btn-outline" href="{{ '/projects.html' | relative_url }}">View Projects</a>
    </div>
  </div>
</section>

<!-- FEATURED POST -->
<section class="featured">
  <div class="wrap">
    <h2>Latest Post</h2>

    {% assign post = site.posts.first %}
    {% if post %}
      <article class="post-card">
        <h3>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h3>
        <p class="post-meta">
          {{ post.date | date: "%B %d, %Y" }}
          {% if post.tags.size > 0 %} • {{ post.tags | join: ", " }}{% endif %}
        </p>
        <p class="post-excerpt">
          {{ post.excerpt | strip_html | truncate: 240 }}
        </p>
        <a class="read-more" href="{{ post.url | relative_url }}">Read more →</a>
      </article>
    {% else %}
      <p class="no-posts">
        No posts yet — create a file in <code>/_posts</code> to get started.
      </p>
    {% endif %}
  </div>
</section>
