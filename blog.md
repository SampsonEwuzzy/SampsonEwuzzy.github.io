---
layout: default
title: Blog
permalink: /blog/
---

<section class="page-header">
  <div class="wrap">
    <h1>Blog</h1>
    <p class="lead">
      Tutorials, research notes, and deep dives into power systems engineering.
    </p>
  </div>
</section>

<section class="blog-list">
  <div class="wrap">
    {% for post in site.posts %}
      <article class="post-card">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p class="post-meta">
          {{ post.date | date: "%B %d, %Y" }}
          {% if post.categories.size > 0 %} • {{ post.categories | join: ", " }}{% endif %}
          {% if post.tags.size > 0 %} • {{ post.tags | join: ", " }}{% endif %}
        </p>
        <p>{{ post.excerpt | strip_html | truncate: 260 }}</p>
        <a class="read-more" href="{{ post.url | relative_url }}">Read more →</a>
      </article>
    {% endfor %}

    {% if site.posts.size == 0 %}
      <p class="no-posts">No posts yet. The journey begins soon!</p>
    {% endif %}
  </div>
</section>

{% if paginator.total_pages > 1 %}
<nav class="pagination">
  <div class="wrap">
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_path | relative_url }}" class="btn btn-outline">← Newer</a>
    {% endif %}
    <span>Page {{ paginator.page }} of {{ paginator.total_pages }}</span>
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path | relative_url }}" class="btn btn-outline">Older →</a>
    {% endif %}
  </div>
</nav>
{% endif %}

