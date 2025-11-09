---
layout: default
title: Search
permalink: /search/
---

<section class="page-header">
  <div class="wrap">
    <h1>Search</h1>
    <p class="lead">Find tutorials, projects, or reflections instantly.</p>
  </div>
</section>

<section class="search-page">
  <div class="wrap">
    <input type="text" id="search-input" placeholder="Type to search..." autofocus>
    <div id="search-results"></div>
  </div>
</section>

<script src="{{ '/assets/js/lunr.js' | relative_url }}"></script>
<script>
  const index = {{ site | jsonify | escape }};
  const documents = {{ site.documents | map: 'title', 'url', 'content' | jsonify }};

  const idx = lunr(function () {
    this.ref('url');
    this.field('title');
    this.field('content');
    documents.forEach(doc => this.add(doc));
  });

  const input = document.getElementById('search-input');
  const results = document.getElementById('search-results');

  input.addEventListener('input', () => {
    const query = input.value.trim();
    if (!query) { results.innerHTML = ''; return; }
    const hits = idx.search(query);
    results.innerHTML = hits.length ? '' : '<p>No results found.</p>';
    hits.forEach(hit => {
      const doc = documents.find(d => d.url === hit.ref);
      const item = `<div class="search-result">
        <h3><a href="${doc.url}">${doc.title}</a></h3>
        <p>${doc.content.substring(0, 150)}...</p>
      </div>`;
      results.innerHTML += item;
    });
  });
</script>

<style>
  #search-input {
    width: 100%; padding: 1rem; font-size: 1.1rem;
    border: 1px solid var(--border); border-radius: var(--radius);
    margin-bottom: 1.5rem;
  }
  .search-result { margin: 1.5rem 0; padding-bottom: 1rem; border-bottom: 1px solid var(--border); }
  .search-result h3 { margin: 0 0 0.5rem; font-size: 1.2rem; }
  .search-result a { color: var(--accent); text-decoration: none; }
  .search-result a:hover { text-decoration: underline; }
</style>