---
layout: default
title: Contact
permalink: /contact/
---

<section class="page-header">
  <div class="wrap">
    <h1>Get in Touch</h1>
    <p class="lead">
      Questions, collaboration ideas, or just want to say hi? Drop me a message.
    </p>
  </div>
</section>

<section class="contact-content">
  <div class="wrap">
    <div class="contact-grid">
      <!-- Contact Info -->
      <div class="contact-info">
        <h3>Connect</h3>
        <ul class="contact-list">
          <li>📧 <a href="mailto:sampson.ewuzie@example.com">sampson.ewuzie@example.com</a></li>
          <li>💼 <a href="https://linkedin.com/in/yourprofile" target="_blank">LinkedIn</a></li>
          <li>🐙 <a href="https://github.com/yourusername" target="_blank">GitHub</a></li>
          <li>✍️ <a href="https://twitter.com/yourhandle" target="_blank">X (Twitter)</a></li>
        </ul>
      </div>

      <!-- Contact Form (Formspree) -->
      <div class="contact-form">
        <form action="https://formspree.io/f/your-form-id" method="POST">
          <label>
            Your Name
            <input type="text" name="name" required placeholder="John Doe">
          </label>

          <label>
            Email
            <input type="email" name="_replyto" required placeholder="john@example.com">
          </label>

          <label>
            Message
            <textarea name="message" rows="5" required placeholder="What’s on your mind?"></textarea>
          </label>

          <button type="submit" class="btn btn-primary">Send Message</button>
        </form>
      </div>
    </div>
  </div>
</section>

<style>
.contact-grid { display: grid; gap: 2rem; grid-template-columns: 1fr 1fr; }
.contact-info ul { list-style: none; padding: 0; }
.contact-info li { margin: .5rem 0; }
.contact-info a { color: var(--accent); text-decoration: none; }
.contact-info a:hover { text-decoration: underline; }
.contact-form label { display: block; margin-top: 1rem; font-weight: 600; }
.contact-form input,
.contact-form textarea {
  width: 100%; padding: .65rem; margin-top: .35rem;
  border: 1px solid var(--border); border-radius: var(--radius);
  font: inherit;
}
.contact-form button { margin-top: 1.5rem; }

@media (max-width: 700px) {
  .contact-grid { grid-template-columns: 1fr; }
}
</style>