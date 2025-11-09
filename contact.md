---
layout: default
title: Contact
permalink: /contact/
---

<!-- Page Header -->
<section class="page-header">
  <div class="wrap">
    <h1>Get in Touch</h1>
    <p class="lead">
      Questions, collaboration ideas, or just want to say hi? Send me an email.
    </p>
  </div>
</section>

<!-- Contact Section -->
<section class="contact-content">
  <div class="wrap">
    <div class="contact-grid">

      <!-- Contact Info -->
      <div class="contact-info">
        <h3>Connect</h3>
        <ul class="contact-list">
          <li> Email: <a href="mailto:sampson.ewuzie@outlook.com">sampson.ewuzie@outlook.com</a></li>
          <li> LinkedIn: <a href="https://www.linkedin.com/in/sampsonewuzie" target="_blank" rel="noopener">LinkedIn</a></li>
          <li> GitHub: <a href="https://github.com/SampsonEwuzzy" target="_blank" rel="noopener">GitHub</a></li>
          <li> X (Twitter): <a href="https://twitter.com/yourhandle" target="_blank" rel="noopener">X</a></li>
        </ul>
      </div>

      <!-- Email Form (mailto) -->
      <div class="contact-form">
        <form id="mailto-form">
          <label>
            Your Name
            <input type="text" id="name" placeholder="John Doe" required>
          </label>

          <label>
            Your Email
            <input type="email" id="email" placeholder="john@example.com" required>
          </label>

          <label>
            Subject
            <input type="text" id="subject" placeholder="Let's collaborate!" value="Website Contact">
          </label>

          <label>
            Message
            <textarea id="message" rows="5" placeholder="What’s on your mind?" required></textarea>
          </label>

          <button type="submit" class="btn btn-primary">Open Email Client</button>
          <p class="form-hint">
            Clicking the button will open your default email app with a pre-filled message.
          </p>
        </form>
      </div>

    </div>
  </div>
</section>

<!-- Inline Styles -->
<style>
  .contact-grid {
    display: grid;
    gap: 2.5rem;
    grid-template-columns: 1fr 1fr;
    margin-top: 1.5rem;
  }
  .contact-info h3 {
    margin-top: 0;
    color: var(--accent, #0b6fb3);
  }
  .contact-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  .contact-list li {
    margin: 0.75rem 0;
    font-size: 1.05rem;
  }
  .contact-list a {
    color: var(--accent, #0b6fb3);
    text-decoration: none;
    font-weight: 500;
  }
  .contact-list a:hover {
    text-decoration: underline;
  }

  .contact-form label {
    display: block;
    margin-top: 1.2rem;
    font-weight: 600;
    color: var(--text, #222);
  }
  .contact-form input,
  .contact-form textarea {
    width: 100%;
    padding: 0.75rem;
    margin-top: 0.4rem;
    border: 1px solid var(--border, #e2e8f0);
    border-radius: 6px;
    font: inherit;
    background: var(--bg, #fff);
    color: var(--text, #222);
  }
  .contact-form input:focus,
  .contact-form textarea:focus {
    outline: none;
    border-color: var(--accent, #0b6fb3);
    box-shadow: 0 0 0 3px rgba(11, 111, 179, 0.15);
  }
  .contact-form button {
    margin-top: 1.5rem;
    width: 100%;
  }
  .form-hint {
    margin-top: 0.75rem;
    font-size: 0.9rem;
    color: var(--muted, #666);
    font-style: italic;
  }

  @media (max-width: 700px) {
    .contact-grid {
      grid-template-columns: 1fr;
      gap: 2rem;
    }
    .contact-form button {
      width: auto;
      padding: 0.75rem 1.5rem;
    }
  }
</style>

<!-- JavaScript: Build mailto: link -->
<script>
  document.getElementById('mailto-form').addEventListener('submit', function(e) {
    e.preventDefault();

    const name = encodeURIComponent(document.getElementById('name').value.trim());
    const email = encodeURIComponent(document.getElementById('email').value.trim());
    const subject = encodeURIComponent(document.getElementById('subject').value.trim());
    const message = encodeURIComponent(document.getElementById('message').value.trim());

    const body = `Hi Sampson,%0D%0A%0D%0AI'm ${name} (${email}).%0D%0A%0D%0A${message}%0D%0A%0D%0ARegards,`;
    const mailtoLink = `mailto:sampson.ewuzie@outlook.com?subject=${subject}&body=${body}`;

    // Open email client
    window.location.href = mailtoLink;
  });
</script>