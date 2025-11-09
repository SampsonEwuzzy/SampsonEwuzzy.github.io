---
layout: default
title: Reflections
permalink: /reflections/
---

<section class="page-header">
  <div class="wrap">
    <h1>Reflections</h1>
    <p class="lead">
      Weekly takeaways from my M.Eng in Power Engineering – what I learned, what surprised me, and how it shapes my thinking.
    </p>
  </div>
</section>

<section class="reflections-list">
  <div class="wrap">
    {% for post in site.posts %}
      {% if post.categories contains 'reflection' %}
        <article class="post-card">
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
          <p class="post-meta">
            {{ post.date | date: "%B %d, %Y" }}
            {% if post.tags.size > 0 %} • {{ post.tags | join: ", " }}{% endif %}
          </p>
          <p>{{ post.excerpt | strip_html | truncate: 260 }}</p>
          <a class="read-more" href="{{ post.url | relative_url }}">Read reflection →</a>
        </article>
      {% endif %}
    {% endfor %}

    {% if site.posts | where: "categories", "reflection" | size == 0 %}
      <p class="no-posts">No reflections yet – check back after the next lecture!</p>
    {% endif %}
  </div>
</section>
