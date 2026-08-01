<template>
  <div class="app-wrapper">
    <!-- Header -->
    <header class="header">
      <div class="container header-inner">
        <div class="logo">BrightPath Technologies</div>
        <nav>
          <a href="#services">Services</a>
          <a href="#portfolio">Work</a>
          <a href="#pricing">Pricing</a>
          <a href="#contact" class="btn btn-secondary nav-btn">Contact Us</a>
        </nav>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
      <div class="container hero-content">
        <h1>Engineering Excellence for the Modern Web</h1>
        <p>We build high-performance, scalable web applications that drive enterprise conversion and growth. Partner with a premium software engineering team.</p>
        <div class="hero-actions">
          <a href="#contact" class="btn">Start a Project</a>
          <a href="#portfolio" class="btn btn-secondary">View Case Studies</a>
        </div>
      </div>
    </section>

    <!-- Trusted By Section -->
    <section class="trusted-by bg-charcoal">
      <div class="container">
        <p class="text-center text-muted mb-4">Trusted by industry leaders</p>
        <div class="logos grid-4">
          <div class="company-logo">Acme Corp</div>
          <div class="company-logo">GlobalTech</div>
          <div class="company-logo">Innovate Inc</div>
          <div class="company-logo">Nexus Systems</div>
        </div>
      </div>
    </section>

    <!-- Services Section -->
    <section id="services">
      <div class="container">
        <div class="section-title">
          <h2>Core Capabilities</h2>
          <p>Delivering robust technical solutions tailored for scale.</p>
        </div>
        <div class="grid-3">
          <div class="card">
            <h3>Custom Web Development</h3>
            <p>Full-stack engineering using modern frameworks. Fast, secure, and built to scale.</p>
          </div>
          <div class="card">
            <h3>Cloud Architecture</h3>
            <p>Resilient infrastructure design and cloud-native application deployment.</p>
          </div>
          <div class="card">
            <h3>System Integration</h3>
            <p>Seamlessly connect legacy systems with modern APIs and microservices.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio" class="bg-charcoal">
      <div class="container">
        <div class="section-title">
          <h2>Case Studies</h2>
          <p>Proven results across complex engineering challenges.</p>
        </div>
        <div class="grid-2">
          <div class="card">
            <h3>FinTech Dashboard</h3>
            <p>A high-frequency trading interface processing 10k+ requests per second.</p>
            <div class="tags">
              <span class="tag">Vue.js</span>
              <span class="tag">Node.js</span>
              <span class="tag">WebSockets</span>
            </div>
          </div>
          <div class="card">
            <h3>E-Commerce Platform</h3>
            <p>Scalable marketplace architecture handling $10M+ in monthly GMV.</p>
            <div class="tags">
              <span class="tag">React</span>
              <span class="tag">GraphQL</span>
              <span class="tag">AWS</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Tech Stack Section -->
    <section id="tech-stack">
      <div class="container">
        <div class="section-title">
          <h2>Technology Stack</h2>
          <p>We leverage industry-standard tools for maximum reliability.</p>
        </div>
        <div class="card text-center">
          <div class="tags-large">
            <span class="tag">Vue.js</span>
            <span class="tag">React</span>
            <span class="tag">TypeScript</span>
            <span class="tag">Node.js</span>
            <span class="tag">Python</span>
            <span class="tag">Go</span>
            <span class="tag">PostgreSQL</span>
            <span class="tag">Redis</span>
            <span class="tag">AWS</span>
            <span class="tag">Docker</span>
            <span class="tag">Kubernetes</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Pricing / Sprints Section -->
    <section id="pricing" class="bg-charcoal">
      <div class="container">
        <div class="section-title">
          <h2>Engagement Models</h2>
          <p>Transparent pricing for high-impact engineering sprints.</p>
        </div>
        <div class="grid-2">
          <div class="card pricing-card">
            <h3>MVP Sprint</h3>
            <div class="price">$15,000<span>/mo</span></div>
            <ul>
              <li>Dedicated Developer</li>
              <li>Weekly Code Reviews</li>
              <li>Basic Infrastructure Setup</li>
            </ul>
            <a href="#contact" class="btn btn-secondary w-100 mt-4">Inquire Now</a>
          </div>
          <div class="card pricing-card featured">
            <h3>Enterprise Scale</h3>
            <div class="price">$45,000<span>/mo</span></div>
            <ul>
              <li>Full Engineering Pod</li>
              <li>Architecture Consulting</li>
              <li>24/7 SLA Support</li>
              <li>Advanced Security Audits</li>
            </ul>
            <a href="#contact" class="btn w-100 mt-4">Inquire Now</a>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials">
      <div class="container">
        <div class="section-title">
          <h2>Client Trust</h2>
          <p>What our enterprise partners say about our engineering.</p>
        </div>
        <div class="grid-2">
          <div class="card">
            <p class="quote">"BrightPath transformed our legacy systems into a modern, scalable architecture. The code quality is exceptional."</p>
            <p class="author">- CTO, GlobalTech</p>
          </div>
          <div class="card">
            <p class="quote">"Professional, transparent, and technically brilliant. They delivered our MVP ahead of schedule."</p>
            <p class="author">- VP Engineering, Nexus Systems</p>
          </div>
        </div>
      </div>
    </section>

    <!-- FAQ Accordion -->
    <section id="faq" class="bg-charcoal">
      <div class="container">
        <div class="section-title">
          <h2>Frequently Asked Questions</h2>
        </div>
        <div class="faq-list">
          <div class="card mb-2">
            <h4>What is your typical project timeline?</h4>
            <p class="mt-2">For MVP sprints, we typically launch within 6-8 weeks. Enterprise scales vary based on scope.</p>
          </div>
          <div class="card mb-2">
            <h4>Do you offer post-launch support?</h4>
            <p class="mt-2">Yes, we provide ongoing maintenance and SLA-backed support contracts.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Form -->
    <section id="contact">
      <div class="container">
        <div class="section-title">
          <h2>Start a Conversation</h2>
          <p>Contact our technical leads to discuss your project requirements.</p>
        </div>
        <div class="contact-form-container card">
          <form @submit.prevent="submitForm">
            <div class="form-group">
              <label class="form-label">Name</label>
              <input type="text" class="form-control" placeholder="Jane Doe" required>
            </div>
            <div class="form-group">
              <label class="form-label">Corporate Email</label>
              <input type="email" class="form-control" placeholder="jane@company.com" required>
            </div>
            <div class="form-group">
              <label class="form-label">Project Details</label>
              <textarea class="form-control" rows="5" placeholder="Tell us about your technical challenges..." required></textarea>
            </div>
            <button type="submit" class="btn w-100">Submit Inquiry</button>
          </form>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="logo">BrightPath Technologies</div>
          <p>&copy; 2026 BrightPath Technologies. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    submitForm() {
      alert('Thank you for your inquiry. Our technical team will reach out shortly.');
    }
  }
}
</script>

<style scoped>
.header {
  padding: var(--spacing-3) 0;
  border-bottom: 1px solid var(--color-border);
  position: sticky;
  top: 0;
  background-color: rgba(2, 6, 23, 0.9);
  backdrop-filter: blur(8px);
  z-index: 100;
}
.header-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.logo {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--color-text);
}
nav a {
  margin-left: var(--spacing-4);
  color: var(--color-text-muted);
  font-weight: 500;
}
nav a:hover {
  color: var(--color-text);
}
.nav-btn {
  padding: var(--spacing-1) var(--spacing-2);
  margin-left: var(--spacing-4);
}
.hero {
  padding: 120px 0;
  text-align: center;
}
.hero h1 {
  font-size: 4rem;
  max-width: 800px;
  margin: 0 auto var(--spacing-4);
}
.hero p {
  font-size: 1.25rem;
  max-width: 600px;
  margin: 0 auto var(--spacing-5);
}
.hero-actions {
  display: flex;
  justify-content: center;
  gap: var(--spacing-3);
}
.bg-charcoal {
  background-color: var(--color-charcoal);
  border-top: 1px solid var(--color-border);
  border-bottom: 1px solid var(--color-border);
}
.text-center { text-align: center; }
.text-muted { color: var(--color-text-muted); }
.mb-4 { margin-bottom: var(--spacing-4); }
.mb-2 { margin-bottom: var(--spacing-2); }
.mt-4 { margin-top: var(--spacing-4); }
.mt-2 { margin-top: var(--spacing-2); }
.w-100 { width: 100%; }
.company-logo {
  text-align: center;
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--color-border);
  padding: var(--spacing-4);
}
.tags {
  margin-top: var(--spacing-3);
}
.tags-large .tag {
  font-size: 1rem;
  padding: 8px 16px;
  margin: var(--spacing-1);
}
.pricing-card {
  display: flex;
  flex-direction: column;
}
.pricing-card.featured {
  border-color: var(--color-blue);
}
.price {
  font-size: 3rem;
  font-weight: 700;
  margin: var(--spacing-3) 0;
}
.price span {
  font-size: 1rem;
  color: var(--color-text-muted);
}
.pricing-card ul {
  list-style: none;
  flex-grow: 1;
}
.pricing-card ul li {
  padding: var(--spacing-2) 0;
  border-bottom: 1px solid var(--color-border);
  color: var(--color-text-muted);
}
.pricing-card ul li:last-child {
  border-bottom: none;
}
.quote {
  font-size: 1.125rem;
  font-style: italic;
  margin-bottom: var(--spacing-3);
}
.author {
  font-weight: 600;
}
.contact-form-container {
  max-width: 600px;
  margin: 0 auto;
}
.footer {
  padding: var(--spacing-6) 0;
  border-top: 1px solid var(--color-border);
  text-align: center;
}
.footer-content p {
  margin-top: var(--spacing-2);
  margin-bottom: 0;
}
@media (max-width: 768px) {
  .hero h1 { font-size: 2.5rem; }
  .hero p { font-size: 1.125rem; }
  .header-inner { flex-direction: column; gap: var(--spacing-3); }
  nav a { margin: 0 var(--spacing-2); }
  .nav-btn { display: none; }
}
</style>
