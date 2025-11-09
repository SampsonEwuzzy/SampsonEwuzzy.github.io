---
layout: default
title: Contact
permalink: /contact/
---

<section class="page-header">
  <div class="wrap">
    <h1>Get in Touch</h1>
    <p class="lead">Send me an email — I reply fast.</p>
  </div>
</section>

<section class="contact-content">
  <div class="wrap">
    <div class="contact-grid">
      <div class="contact-info">
        <h3>Connect</h3>
        <ul class="contact-list">
          <li>Email: <a href="mailto:sampson.ewuzie@outlook.com">sampson.ewuzie@outlook.com</a></li>
          <li>LinkedIn: <a href="https://www.linkedin.com/in/sampsonewuzie" target="_blank">LinkedIn</a></li>
          <li>GitHub: <a href="https://github.com/SampsonEwuzzy" target="_blank">GitHub</a></li>
        </ul>
      </div>
      <div class="contact-form">
        <form id="mailto-form">
          <label>Your Name <input type="text" id="name" required></label>
          <label>Your Email <input type="email" id="email" required></label>
          <label>Message <textarea id="message" rows="5" required></textarea></label>
          <button type="submit" class="btn btn-primary">Open Email</button>
        </form>
      </div>
    </div>
  </div>
</section>

<script>
  document.getElementById('mailto-form').addEventListener('submit', function(e) {
    e.preventDefault();
    const name = encodeURIComponent(document.getElementById('name').value);
    const email = encodeURIComponent(document.getElementById('email').value);
    const message = encodeURIComponent(document.getElementById('message').value);
    const body = `Hi Sampson,%0D%0A%0D%0AI'm ${name} (${email}).%0D%0A%0D%0A${message}`;
    window.location.href = `mailto:sampson.ewuzie@outlook.com?subject=Website Contact&body=${body}`;
  });
</script>