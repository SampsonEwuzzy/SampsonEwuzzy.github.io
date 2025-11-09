---
layout: default
title: "Blog"
permalink: /blog/
---

# Blog / Tutorials

{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="meta">Published on {{ post.date | date: "%B %-d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncate: 220 }}</p>
  </article>
  <hr>
{% endfor %}
