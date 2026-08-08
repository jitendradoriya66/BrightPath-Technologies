<template>
  <div class="app-shell" :class="{'no-scroll': mobileMenuOpen}">
    <a class="skip-link" href="#main">Skip to content</a>

    <header class="topbar" :class="{ scrolled: isScrolled }">
      <div class="container topbar-inner">
        <a class="brand" href="#main">BrightPath<span>Technologies</span></a>
        <nav class="site-nav" aria-label="Primary navigation">
          <a href="#services">Services</a>
          <a href="#work">Work</a>
          <a href="#process">Process</a>
          <a href="#contact">Contact</a>
        </nav>
        <div class="header-actions">
          <a class="btn btn-primary nav-cta" href="#contact">Book a call</a>
          <button class="mobile-toggle" @click="toggleMobileMenu" :aria-expanded="mobileMenuOpen.toString()" aria-controls="mobile-menu" aria-label="Toggle navigation">
            <div class="hamburger" :class="{ 'is-active': mobileMenuOpen }">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </button>
        </div>
      </div>
      <transition name="fade-blur">
        <div v-if="mobileMenuOpen" class="mobile-menu-overlay" @click="closeMobileMenu">
          <div class="mobile-nav" @click.stop id="mobile-menu" ref="mobileNav">
            <div class="mobile-nav-links">
              <a href="#services" @click="closeMobileMenu" style="--delay: 0.1s">Services</a>
              <a href="#work" @click="closeMobileMenu" style="--delay: 0.2s">Work</a>
              <a href="#process" @click="closeMobileMenu" style="--delay: 0.3s">Process</a>
              <a href="#contact" @click="closeMobileMenu" style="--delay: 0.4s">Contact</a>
              <a href="#contact" class="btn btn-primary mobile-nav-cta" @click="closeMobileMenu" style="--delay: 0.5s">Book a call</a>
            </div>
          </div>
        </div>
      </transition>
    </header>

    <main id="main">
      <section class="hero section" aria-labelledby="hero-heading">
        <div class="container hero-grid">
          <div class="hero-copy reveal">
            <p class="eyebrow">Premium software for ambitious teams</p>
            <h1 id="hero-heading">We build custom web apps, AI platforms, and automation systems that help teams launch faster and grow with confidence.</h1>
            <p class="hero-text">From concept to launch-ready product, we shape polished digital experiences around real business outcomes: faster onboarding, less manual work, and clearer momentum for the people using them.</p>
            <div class="hero-actions">
              <a class="btn btn-primary" href="#contact">Book a free consultation <span aria-hidden="true">↗</span></a>
              <a class="btn btn-secondary" href="#work">See case studies</a>
            </div>
            <div class="hero-trust" aria-label="Trust indicators">
              <div class="trust-pill">Custom web apps</div>
              <div class="trust-pill">AI automation</div>
              <div class="trust-pill">Fast delivery</div>
            </div>
            <div class="hero-logos" aria-label="Technology stack">
              <span>React</span>
              <span>Vue</span>
              <span>Django</span>
              <span>Python</span>
              <span>Docker</span>
              <span>AWS</span>
            </div>
          </div>

          <div class="hero-visual reveal" aria-hidden="true">
            <div class="dashboard-shell">
              <div class="dashboard-topbar">
                <div class="topbar-dots">
                  <span></span>
                  <span></span>
                  <span></span>
                </div>
                <div class="topbar-title">Product Studio</div>
              </div>
              <div class="dashboard-body">
                <aside class="dashboard-sidebar">
                  <div class="sidebar-item active">Overview</div>
                  <div class="sidebar-item">Roadmap</div>
                  <div class="sidebar-item">CRM</div>
                </aside>
                <div class="dashboard-content">
                  <div class="dashboard-heading">
                    <div>
                      <p class="mini-label">Launch readiness</p>
                      <h3>Weekly momentum</h3>
                    </div>
                    <span class="status-pill">+18.2%</span>
                  </div>
                  <div class="dashboard-grid">
                    <div class="dashboard-card wide">
                      <div class="card-label">ARR trend</div>
                      <div class="chart-bars">
                        <span></span>
                        <span></span>
                        <span></span>
                        <span></span>
                        <span></span>
                      </div>
                    </div>
                    <div class="dashboard-card">3.2x conversion</div>
                    <div class="dashboard-card">24/7 support</div>
                    <div class="dashboard-card wide secondary">
                      <div class="card-label">Team pulse</div>
                      <ul>
                        <li>Roadmap sync</li>
                        <li>Client feedback</li>
                        <li>QA complete</li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="floating-pill one">Design systems</div>
            <div class="floating-pill two">Fast delivery</div>
          </div>
        </div>
      </section>

      <!-- Logo Strip (Marquee) -->
      <section class="marquee-section border-y">
        <div class="marquee-container">
          <div class="marquee-track">
            <span v-for="n in 3" :key="n" class="marquee-group">
              <span v-for="logo in logos" :key="logo + n" class="marquee-item">{{ logo }}</span>
            </span>
          </div>
        </div>
      </section>

      <!-- Services (Bento) -->
      <section id="services" class="section bg-soft">
        <div class="container">
          <div class="section-heading mb-8">
            <p class="eyebrow">Capabilities</p>
            <h2>End-to-end engineering excellence</h2>
            <p class="subtitle">We deliver premium software solutions designed to accelerate growth, optimize operations, and elevate customer experiences.</p>
          </div>
          
          <div class="bento-grid">
            <div class="bento-card bento-primary">
              <div class="bento-content">
                <h3>Enterprise Web Applications</h3>
                <p>Scalable, secure, and performant web applications built with modern frameworks. We focus on maintainability, elegant architecture, and seamless user experiences that drive business value.</p>
                <ul class="bento-list">
                  <li>React & Vue ecosystems</li>
                  <li>Microservices architecture</li>
                  <li>High-availability infrastructure</li>
                </ul>
                <a href="#about" class="link-cta">Explore capability <span>&rarr;</span></a>
              </div>
            </div>
            
            <div class="bento-card">
              <div class="bento-content">
                <h3>AI & Automation Systems</h3>
                <p>Integrating intelligent automation into your workflows to reduce manual overhead and unlock new capabilities.</p>
                <a href="#about" class="link-cta">Explore capability <span>&rarr;</span></a>
              </div>
            </div>

            <div class="bento-card">
              <div class="bento-content">
                <h3>Cloud Native Architecture</h3>
                <p>Resilient cloud infrastructure utilizing AWS, Docker, and Kubernetes for maximum uptime.</p>
                <a href="#about" class="link-cta">Explore capability <span>&rarr;</span></a>
              </div>
            </div>
            
            <div class="bento-card bento-wide">
              <div class="bento-content">
                <h3>Product Design & Strategy</h3>
                <p>We bridge the gap between business objectives and technical execution. Our design process ensures that every feature we build solves a real user problem, wrapped in a polished, intuitive interface.</p>
                <a href="#about" class="link-cta">Explore capability <span>&rarr;</span></a>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Why Choose Us -->
      <section id="about" class="section border-y">
        <div class="container">
          <div class="trust-block">
            <div class="trust-header">
              <h2>Built on trust, quality, and rigorous process</h2>
              <p>We don't just write code; we partner with you to engineer success. Our metrics speak for our commitment to excellence.</p>
            </div>
            <div class="trust-metrics">
              <div class="metric-item">
                <span class="metric-val">100%</span>
                <span class="metric-label">In-house engineering</span>
              </div>
              <div class="metric-item">
                <span class="metric-val">&lt;24h</span>
                <span class="metric-label">Response time</span>
              </div>
              <div class="metric-item">
                <span class="metric-val">0</span>
                <span class="metric-label">Missed deadlines</span>
              </div>
              <div class="metric-item">
                <span class="metric-val">99.9%</span>
                <span class="metric-label">Uptime delivered</span>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Case Studies -->
      <section id="work" class="section">
        <div class="container">
          <div class="section-heading mb-8">
            <p class="eyebrow">Selected Work</p>
            <h2>Proven results in production</h2>
          </div>

          <div class="work-showcase">
            <div class="work-row">
              <div class="work-info">
                <h3>Fintech Operations Platform</h3>
                <p><strong>Problem:</strong> Fragmented data systems causing 2-day delays in financial reporting.</p>
                <p><strong>Solution:</strong> A centralized real-time dashboard unifying 5 disparate APIs with custom reconciliation logic.</p>
                <div class="tech-badges">
                  <span>Vue.js</span>
                  <span>Node.js</span>
                  <span>PostgreSQL</span>
                </div>
                <div class="work-results">
                  <div class="res"><strong>98%</strong> reduction in manual entry</div>
                  <div class="res"><strong>2x</strong> faster reporting</div>
                </div>
              </div>
              <div class="work-visual-mockup">
                <div class="mockup-placeholder">Dashboard Mockup</div>
              </div>
            </div>

            <div class="work-row reverse">
              <div class="work-info">
                <h3>AI-Powered SaaS Onboarding</h3>
                <p><strong>Problem:</strong> High drop-off rates during complex enterprise software configuration.</p>
                <p><strong>Solution:</strong> An intelligent conversational onboarding flow utilizing LLMs to auto-configure user environments.</p>
                <div class="tech-badges">
                  <span>React</span>
                  <span>Python</span>
                  <span>OpenAI</span>
                </div>
                <div class="work-results">
                  <div class="res"><strong>+45%</strong> activation rate</div>
                  <div class="res"><strong>3x</strong> lower support volume</div>
                </div>
              </div>
              <div class="work-visual-mockup">
                <div class="mockup-placeholder">Onboarding UI Mockup</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Process -->
      <section id="process" class="section bg-soft border-y">
        <div class="container">
          <div class="section-heading text-center mb-8">
            <p class="eyebrow">Our Methodology</p>
            <h2>A disciplined approach to delivery</h2>
          </div>
          <div class="process-timeline">
            <div v-for="(step, i) in processSteps" :key="i" class="process-step">
              <div class="step-num">0{{ i + 1 }}</div>
              <h4>{{ step.title }}</h4>
              <p>{{ step.desc }}</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Technologies -->
      <section class="section">
        <div class="container">
          <div class="section-heading mb-6">
            <p class="eyebrow">Technology Stack</p>
            <h2>Enterprise-grade tools</h2>
          </div>
          <div class="tech-ecosystem">
            <div class="tech-category" v-for="(cat, name) in technologies" :key="name">
              <h4>{{ name }}</h4>
              <div class="tech-tags">
                <span v-for="tech in cat" :key="tech">{{ tech }}</span>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Testimonials -->
      <section class="section bg-soft border-y">
        <div class="container">
          <div class="section-heading mb-6">
            <h2>Client success stories</h2>
          </div>
          <div class="testimonial-grid">
            <div v-for="(t, i) in testimonials" :key="i" class="testimonial-box">
              <div class="stars">★★★★★</div>
              <p class="quote">"{{ t.quote }}"</p>
              <div class="author">
                <div class="avatar"></div>
                <div>
                  <strong>{{ t.name }}</strong>
                  <span>{{ t.role }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- FAQ Accordion -->
      <section class="section">
        <div class="container">
          <div class="section-heading mb-6">
            <h2>Frequently asked questions</h2>
          </div>
          <div class="faq-list">
            <details v-for="(faq, i) in faqs" :key="i" class="faq-item">
              <summary class="faq-question">{{ faq.q }} <span class="icon">+</span></summary>
              <div class="faq-answer"><p>{{ faq.a }}</p></div>
            </details>
          </div>
        </div>
      </section>

      <!-- Contact / CTA -->
      <section id="contact" class="section cta-section bg-dark text-light">
        <div class="container cta-grid">
          <div class="cta-copy">
            <h2>Have an idea? Let's build it.</h2>
            <p>Get in touch for a technical consultation. We review your requirements and provide a clear roadmap within 24 hours.</p>
            <ul class="cta-benefits">
              <li>✓ NDA protected</li>
              <li>✓ No commitment required</li>
              <li>✓ Technical feasibility review</li>
            </ul>
          </div>
          <div class="cta-form-container">
            <form class="cta-form" @submit.prevent="submitForm">
              <div class="form-row">
                <label>Name</label>
                <input type="text" required placeholder="Jane Doe" />
              </div>
              <div class="form-row">
                <label>Work Email</label>
                <input type="email" required placeholder="jane@company.com" />
              </div>
              <div class="form-row">
                <label>Project Details</label>
                <textarea rows="4" required placeholder="Tell us about what you're building..."></textarea>
              </div>
              <button type="submit" class="btn btn-primary w-full">Request Consultation</button>
            </form>
          </div>
        </div>
      </section>
    </main>

    <!-- Footer -->
    <footer class="site-footer">
      <div class="container footer-layout">
        <div class="footer-brand">
          <a class="brand" href="#main">BrightPath<span>Technologies</span></a>
          <p>Premium software engineering and design for ambitious companies scaling their digital footprint.</p>
        </div>
        <div class="footer-links">
          <h4>Services</h4>
          <a href="#services">Web Applications</a>
          <a href="#services">AI Automation</a>
          <a href="#services">Cloud Architecture</a>
          <a href="#services">Product Design</a>
        </div>
        <div class="footer-links">
          <h4>Company</h4>
          <a href="#work">Work</a>
          <a href="#process">Process</a>
            <a href="#about">About</a>
          <a href="#contact">Contact</a>
        </div>
        <div class="footer-contact">
          <h4>Subscribe</h4>
          <p>Get technical insights delivered monthly.</p>
          <div class="newsletter">
            <input type="email" placeholder="Email address" />
            <button class="btn btn-primary">Join</button>
          </div>
        </div>
      </div>
      <div class="container footer-bottom">
        <p>&copy; 2026 BrightPath Technologies. All rights reserved.</p>
        <div class="footer-legal">
          <a href="#main">Privacy Policy</a>
          <a href="#contact">Terms of Service</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      mobileMenuOpen: false,
      isScrolled: false,
      logos: ['Acme Corp', 'GlobalTech', 'Nexus', 'Vertex', 'Zephyr', 'Quantum', 'Starlight'],
      processSteps: [
        { title: 'Discovery', desc: 'Understanding your business logic, constraints, and objectives.' },
        { title: 'Architecture', desc: 'Designing scalable infrastructure and data models.' },
        { title: 'Prototyping', desc: 'Rapid UI/UX iteration to validate workflows.' },
        { title: 'Development', desc: 'Rigorous engineering with automated testing.' },
        { title: 'Deployment', desc: 'Zero-downtime releases and CI/CD pipelines.' },
        { title: 'Maintenance', desc: 'Ongoing monitoring and proactive optimizations.' }
      ],
      technologies: {
        'Frontend': ['React', 'Vue', 'TypeScript', 'Tailwind', 'Next.js'],
        'Backend': ['Node.js', 'Python', 'Django', 'Go', 'GraphQL'],
        'Database': ['PostgreSQL', 'MongoDB', 'Redis', 'Elasticsearch'],
        'Cloud & DevOps': ['AWS', 'Docker', 'Kubernetes', 'GitHub Actions']
      },
      testimonials: [
        { quote: "Their technical depth and design precision completely transformed our internal tooling.", name: "Sarah Jenkins", role: "CTO, Finova" },
        { quote: "BrightPath delivered our MVP 3 weeks ahead of schedule with zero critical bugs.", name: "David Chen", role: "Founder, ScaleAI" },
        { quote: "A true engineering partner. They didn't just build what we asked, they built what we needed.", name: "Elena Rostova", role: "VP Product, Nexus" }
      ],
      faqs: [
        { q: "How do you handle project pricing?", a: "We provide detailed scoping during discovery, offering both fixed-bid for defined scopes and T&M for agile, evolving projects." },
        { q: "Do you maintain the software after launch?", a: "Yes, we offer flexible SLA-backed maintenance and continuous improvement retainers." },
        { q: "How do you ensure code quality?", a: "We enforce strict PR reviews, comprehensive automated testing (unit/integration/E2E), and CI/CD pipelines on every project." }
      ]
    }
  },
  mounted() {
    this.handleScroll()
    window.addEventListener('scroll', this.handleScroll, { passive: true })
    window.addEventListener('resize', this.handleResize, { passive: true })
    window.addEventListener('keydown', this.handleKeydown)
    this.observeReveal()
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll)
    window.removeEventListener('resize', this.handleResize)
    window.removeEventListener('keydown', this.handleKeydown)
    if (this.revealObserver) this.revealObserver.disconnect()
  },
  watch: {
    mobileMenuOpen(val) {
      if (val) {
        document.body.classList.add('no-scroll')
        this.$nextTick(() => {
          const firstLink = this.$refs.mobileNav.querySelector('a')
          if (firstLink) firstLink.focus()
        })
      } else {
        document.body.classList.remove('no-scroll')
      }
    }
  },
  methods: {
    toggleMobileMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen
    },
    closeMobileMenu() {
      this.mobileMenuOpen = false
    },
    handleKeydown(e) {
      if (e.key === 'Escape' && this.mobileMenuOpen) {
        this.closeMobileMenu()
      }
      if (this.mobileMenuOpen && e.key === 'Tab') {
        const focusableElements = this.$refs.mobileNav.querySelectorAll('a, button')
        const firstElement = focusableElements[0]
        const lastElement = focusableElements[focusableElements.length - 1]
        
        if (e.shiftKey) {
          if (document.activeElement === firstElement) {
            lastElement.focus()
            e.preventDefault()
          }
        } else {
          if (document.activeElement === lastElement) {
            firstElement.focus()
            e.preventDefault()
          }
        }
      }
    },
    handleScroll() {
      this.isScrolled = window.scrollY > 10
    },
    handleResize() {
      if (window.innerWidth > 768 && this.mobileMenuOpen) {
        this.closeMobileMenu()
      }
    },
    submitForm() {
      alert('Thanks for your inquiry. Our team will contact you shortly.')
    },
    observeReveal() {
      if (typeof window === 'undefined' || !('IntersectionObserver' in window)) return
      this.revealObserver = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible')
            this.revealObserver.unobserve(entry.target)
          }
        })
      }, { threshold: 0.1 })
      document.querySelectorAll('.reveal').forEach((item) => this.revealObserver.observe(item))
    }
  }
}
</script>

<style>
/* Base Styles & Utilities */
.bg-soft { background: var(--surface-soft); }
.bg-dark { background: var(--primary); color: #fff; }
.text-light { color: #fff; }
.border-y { border-top: 1px solid var(--border); border-bottom: 1px solid var(--border); }
.mb-6 { margin-bottom: var(--space-6); }
.mb-8 { margin-bottom: var(--space-8); }
.text-center { text-align: center; }
.w-full { width: 100%; }

/* Skip Link */
.skip-link {
  position: absolute;
  top: -40px;
  left: 16px;
  background: var(--primary);
  color: #fff;
  padding: 8px 16px;
  z-index: 999;
}
.skip-link:focus { top: 16px; }

/* Topbar */
.topbar {
  position: sticky;
  top: 0;
  z-index: 100;
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid transparent;
  transition: var(--trans);
}
.topbar.scrolled {
  border-bottom-color: var(--border);
  box-shadow: 0 4px 12px rgba(0,0,0,0.05);
}
.topbar-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 72px;
}
.brand {
  font-weight: 700;
  font-size: 1.25rem;
  letter-spacing: -0.02em;
}
.brand span { color: var(--accent); }
.site-nav { display: flex; gap: var(--space-4); }
.site-nav a { font-weight: 500; transition: color 0.2s; }
.site-nav a:hover { color: var(--primary); }
@media (max-width: 768px) {
  .site-nav { display: none; }
}
.header-actions {
  display: flex;
  align-items: center;
  gap: var(--space-2);
}
.mobile-toggle {
  display: none;
  z-index: 101;
  padding: 8px;
  margin-right: -8px;
}
@media (max-width: 768px) {
  .mobile-toggle { display: block; }
  .nav-cta {
    padding: 8px 12px;
    font-size: 0.875rem;
    white-space: nowrap;
    display: inline-flex;
    align-items: center;
    justify-content: center;
  }
}
.hamburger {
  width: 24px;
  height: 20px;
  position: relative;
}
.hamburger span {
  display: block;
  position: absolute;
  height: 2px;
  width: 100%;
  background: var(--primary);
  border-radius: 2px;
  opacity: 1;
  left: 0;
  transition: .25s ease-in-out;
}
.hamburger span:nth-child(1) { top: 0px; }
.hamburger span:nth-child(2) { top: 9px; }
.hamburger span:nth-child(3) { top: 18px; }
.hamburger.is-active span:nth-child(1) { top: 9px; transform: rotate(135deg); }
.hamburger.is-active span:nth-child(2) { opacity: 0; left: -20px; }
.hamburger.is-active span:nth-child(3) { top: 9px; transform: rotate(-135deg); }

/* Mobile Menu Overlay */
.mobile-menu-overlay {
  position: fixed;
  inset: 0;
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(24px);
  -webkit-backdrop-filter: blur(24px);
  z-index: 300;
  display: flex;
  align-items: flex-start;
  justify-content: center;
  padding: calc(4.75rem + 1rem) 1rem 1rem;
}
.fade-blur-enter-active,
.fade-blur-leave-active {
  transition: opacity 0.4s ease, backdrop-filter 0.4s ease, -webkit-backdrop-filter 0.4s ease;
}
.fade-blur-enter-from,
.fade-blur-leave-to {
  opacity: 0;
  backdrop-filter: blur(0px);
  -webkit-backdrop-filter: blur(0px);
}
.mobile-nav-links {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: var(--space-4);
}
.mobile-nav {
  width: min(100%, 26rem);
  padding: 2rem 1.5rem 2.5rem;
  border-radius: 28px;
  background: rgba(255, 255, 255, 0.96);
  border: 1px solid rgba(148, 163, 184, 0.18);
  box-shadow: var(--shadow-lg);
}
.mobile-nav-links a {
  font-size: 2rem;
  font-weight: 600;
  color: var(--primary);
  opacity: 0;
  transform: translateY(20px);
  animation: slideUp 0.4s forwards;
  animation-delay: var(--delay);
}
.mobile-nav-links .mobile-nav-cta {
  font-size: 1.125rem;
  margin-top: var(--space-2);
  color: #fff;
}
@keyframes slideUp {
  to { opacity: 1; transform: translateY(0); }
}

/* Hero Section */
.hero {
  padding-top: var(--space-8);
  padding-bottom: var(--space-10);
}
.hero-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: var(--space-6);
  align-items: center;
}
@media (max-width: 992px) {
  .hero-grid { grid-template-columns: 1fr; }
}
    display: none;
.hero-logos { display: flex; gap: var(--space-2); flex-wrap: wrap; }
.hero-logos span { font-size: 0.875rem; font-weight: 600; padding: 4px 12px; background: var(--surface-soft); border-radius: 4px; }
.hero-visual { position: relative; }
.dashboard-shell { border: 1px solid var(--border); border-radius: 8px; background: #fff; box-shadow: 0 24px 48px rgba(0,0,0,0.05); padding: var(--space-2); }
.dashboard-topbar { display: flex; justify-content: space-between; border-bottom: 1px solid var(--border); padding-bottom: var(--space-2); margin-bottom: var(--space-2); }
.topbar-dots span { display: inline-block; width: 10px; height: 10px; background: var(--border-strong); border-radius: 50%; margin-right: 6px; }
.dashboard-body { display: grid; grid-template-columns: 100px 1fr; gap: var(--space-2); }
.sidebar-item { font-size: 0.75rem; padding: 4px 8px; margin-bottom: 4px; border-radius: 4px; }
.sidebar-item.active { background: var(--surface-alt); font-weight: 600; }
.dashboard-heading { display: flex; justify-content: space-between; align-items: center; margin-bottom: var(--space-2); }
.status-pill { font-size: 0.75rem; background: #ecfdf5; color: #059669; padding: 2px 8px; border-radius: 999px; font-weight: 600; }
.dashboard-grid { display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-2); }
.dashboard-card { border: 1px solid var(--border); padding: var(--space-2); border-radius: 6px; font-size: 0.875rem; font-weight: 600; }
.dashboard-card.wide { grid-column: span 2; }
.card-label { font-size: 0.75rem; color: var(--text-muted); text-transform: uppercase; }
.chart-bars { display: flex; align-items: flex-end; gap: 4px; height: 40px; margin-top: 8px; }
.chart-bars span { flex: 1; background: var(--primary); border-radius: 2px 2px 0 0; }
.chart-bars span:nth-child(1) { height: 40%; }
.chart-bars span:nth-child(2) { height: 60%; }
.chart-bars span:nth-child(3) { height: 50%; }
.chart-bars span:nth-child(4) { height: 80%; }
.chart-bars span:nth-child(5) { height: 100%; }
.floating-pill { position: absolute; padding: 8px 16px; background: #fff; border: 1px solid var(--border); box-shadow: 0 4px 12px rgba(0,0,0,0.05); border-radius: 999px; font-size: 0.875rem; font-weight: 600; z-index: 10; }
.floating-pill.one { top: -20px; right: 20px; }
.floating-pill.two { bottom: -20px; left: -20px; }

/* Marquee */
.marquee-section { padding: var(--space-3) 0; overflow: hidden; background: #fafafa; }
.marquee-container { display: flex; white-space: nowrap; }
.marquee-track { display: flex; animation: marquee 20s linear infinite; }
.marquee-group { display: flex; gap: var(--space-6); padding-right: var(--space-6); }
.marquee-item { font-size: 1.25rem; font-weight: 700; color: var(--border-strong); }
@keyframes marquee { 0% { transform: translateX(0); } 100% { transform: translateX(-33.33%); } }

/* Bento Grid */
.bento-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: var(--space-3); }
.bento-card { border: 1px solid var(--border); border-radius: 16px; padding: var(--space-4); background: #fff; transition: var(--trans); }
.bento-card:hover { border-color: var(--border-strong); box-shadow: 0 8px 32px rgba(0,0,0,0.06); transform: translateY(-2px); }
.bento-primary { grid-column: span 2; grid-row: span 2; background: var(--surface-alt); border: none; }
.bento-wide { grid-column: span 2; }
@media (max-width: 992px) { .bento-grid, .bento-primary, .bento-wide { grid-template-columns: 1fr; grid-column: span 1; grid-row: span 1; } }
.bento-content h3 { margin-bottom: var(--space-2); }
.bento-list { margin: var(--space-2) 0; padding-left: var(--space-3); font-weight: 500; }
.link-cta { display: inline-flex; align-items: center; gap: 4px; font-weight: 600; color: var(--primary); margin-top: var(--space-2); }
.link-cta span { transition: transform 0.2s; }
.link-cta:hover span { transform: translateX(4px); }

/* Trust Block */
.trust-block { display: grid; grid-template-columns: 1fr 1.5fr; gap: var(--space-6); align-items: center; }
@media (max-width: 768px) { .trust-block { grid-template-columns: 1fr; } }
.trust-metrics { display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-4); }
.metric-item { border-left: 2px solid var(--primary); padding-left: var(--space-2); }
.metric-val { display: block; font-size: 2.5rem; font-weight: 700; color: var(--primary); line-height: 1; margin-bottom: 4px; }
.metric-label { font-size: 0.9rem; font-weight: 500; }

/* Case Studies */
.work-showcase { display: grid; gap: var(--space-8); }
.work-row { display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-6); align-items: center; }
.work-row.reverse .work-info { order: 2; }
.work-row.reverse .work-visual-mockup { order: 1; }
@media (max-width: 768px) { .work-row, .work-row.reverse { grid-template-columns: 1fr; } .work-row.reverse .work-info { order: 1; } .work-row.reverse .work-visual-mockup { order: 2; } }
.tech-badges { display: flex; gap: var(--space-1); margin-bottom: var(--space-3); flex-wrap: wrap; }
.tech-badges span { font-size: var(--text-sm); font-weight: 600; padding: 4px 12px; border: 1px solid var(--border); border-radius: 8px; }
.work-results { display: flex; gap: var(--space-4); border-top: 1px solid var(--border); padding-top: var(--space-3); margin-top: var(--space-3); }
.work-results .res { font-size: var(--text-base); }
.work-results strong { font-size: var(--text-xl); color: var(--primary); display: block; }
.work-visual-mockup { background: var(--surface-alt); border-radius: 16px; height: 320px; display: flex; align-items: center; justify-content: center; border: 1px solid var(--border); }
.mockup-placeholder { font-weight: 600; color: var(--border-strong); }

/* Process */
.process-timeline { display: grid; grid-template-columns: repeat(3, 1fr); gap: var(--space-4); }
@media (max-width: 768px) { .process-timeline { grid-template-columns: 1fr; } }
.process-step { border: 1px solid var(--border); padding: var(--space-4); border-radius: 16px; position: relative; background: #fff; }
.step-num { font-size: var(--text-sm); font-weight: 700; color: var(--border-strong); margin-bottom: var(--space-2); }

/* Tech */
.tech-ecosystem { display: grid; grid-template-columns: repeat(4, 1fr); gap: var(--space-4); }
@media (max-width: 992px) { .tech-ecosystem { grid-template-columns: repeat(2, 1fr); } }
@media (max-width: 480px) { .tech-ecosystem { grid-template-columns: 1fr; } }
.tech-category h4 { margin-bottom: var(--space-2); font-size: 1rem; border-bottom: 1px solid var(--border); padding-bottom: 8px; }
.tech-tags { display: flex; flex-wrap: wrap; gap: var(--space-1); }
.tech-tags span { font-size: 0.85rem; padding: 4px 8px; background: var(--surface-alt); border-radius: 4px; }

/* Testimonials */
.testimonial-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: var(--space-4); }
@media (max-width: 992px) { .testimonial-grid { grid-template-columns: 1fr; } }
.testimonial-box { border: 1px solid var(--border); padding: var(--space-4); border-radius: 16px; background: #fff; }
.stars { color: #eab308; margin-bottom: var(--space-2); font-size: var(--text-xl); }
.quote { font-size: var(--text-lg); font-weight: 500; color: var(--primary); margin-bottom: var(--space-4); }
.author { display: flex; align-items: center; gap: var(--space-2); }
.avatar { width: 48px; height: 48px; background: var(--surface-alt); border-radius: 50%; }
.author strong { display: block; font-size: var(--text-base); }
.author span { font-size: var(--text-sm); color: var(--text-muted); }

/* FAQ */
.faq-list { border-top: 1px solid var(--border); }
.faq-item { border-bottom: 1px solid var(--border); padding: var(--space-3) 0; }
.faq-question { font-weight: 600; font-size: 1.1rem; cursor: pointer; display: flex; justify-content: space-between; align-items: center; list-style: none; outline: none; }
.faq-question::-webkit-details-marker { display: none; }
.faq-question .icon { font-size: 1.5rem; color: var(--border-strong); transition: var(--trans); }
.faq-item[open] .icon { transform: rotate(45deg); }
.faq-answer { padding-top: var(--space-2); color: var(--text-muted); }

/* CTA */
.cta-section { padding: var(--space-10) 0; }
.cta-grid { display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-8); align-items: center; }
@media (max-width: 768px) { .cta-grid { grid-template-columns: 1fr; } }
.cta-copy h2 { color: #fff; margin-bottom: var(--space-2); }
.cta-copy p { font-size: var(--text-lg); opacity: 0.9; margin-bottom: var(--space-4); }
.cta-benefits { list-style: none; display: grid; gap: var(--space-1); font-weight: 500; }
.cta-form-container { background: #fff; padding: var(--space-5); border-radius: 16px; color: var(--text); }
.cta-form .form-row { margin-bottom: var(--space-3); }
.cta-form label { display: block; font-weight: 600; font-size: var(--text-sm); margin-bottom: 8px; }
.cta-form input, .cta-form textarea { width: 100%; border: 1px solid var(--border-strong); padding: 16px; border-radius: 8px; font: inherit; background: var(--surface-soft); transition: var(--trans); color: var(--text); }
.cta-form input:focus, .cta-form textarea:focus { border-color: var(--primary); outline: none; background: #fff; box-shadow: 0 0 0 2px rgba(15, 23, 42, 0.1); }

/* Footer */
.site-footer { padding: var(--space-10) 0 var(--space-4); background: var(--surface-alt); border-top: 1px solid var(--border); }
.footer-layout { display: grid; grid-template-columns: 2fr 1fr 1fr 1.5fr; gap: var(--space-6); margin-bottom: var(--space-8); }
@media (max-width: 992px) { .footer-layout { grid-template-columns: 1fr 1fr; } }
@media (max-width: 480px) { .footer-layout { grid-template-columns: 1fr; } }
.footer-brand p { margin-top: var(--space-2); font-size: 0.95rem; }
.footer-links h4, .footer-contact h4 { margin-bottom: var(--space-3); font-size: 1rem; }
.footer-links a { display: block; margin-bottom: var(--space-2); font-size: 0.95rem; font-weight: 500; transition: color 0.2s; }
.footer-links a:hover { color: var(--primary); }
.newsletter { display: flex; gap: var(--space-1); margin-top: var(--space-2); }
.newsletter input { flex: 1; border: 1px solid var(--border); padding: 8px 12px; border-radius: 4px; }
.footer-bottom { display: flex; justify-content: space-between; align-items: center; border-top: 1px solid var(--border); padding-top: var(--space-4); font-size: 0.9rem; }
@media (max-width: 768px) { .footer-bottom { flex-direction: column; gap: var(--space-2); text-align: center; } }
.footer-legal { display: flex; gap: var(--space-3); }

/* Reveal Animation */
.reveal { opacity: 0; transform: translateY(20px); transition: opacity 0.6s ease-out, transform 0.6s ease-out; }
.reveal.visible { opacity: 1; transform: translateY(0); }

.app-shell {
  position: relative;
  overflow-x: clip;
}

.app-shell::before {
  content: '';
  position: fixed;
  inset: 0;
  pointer-events: none;
  background:
    radial-gradient(circle at 20% 10%, rgba(37, 99, 235, 0.12), transparent 28%),
    radial-gradient(circle at 80% 0%, rgba(15, 23, 42, 0.08), transparent 22%);
  z-index: -1;
}

.topbar {
  background: rgba(245, 247, 251, 0.82);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
}

.topbar.scrolled {
  box-shadow: var(--shadow-sm);
}

.topbar-inner {
  min-height: 4.75rem;
}

.brand {
  display: inline-flex;
  align-items: baseline;
  gap: 0.2em;
}

.site-nav {
  gap: 1.75rem;
}

.site-nav a {
  position: relative;
  font-weight: 600;
  color: var(--text-muted);
}

.site-nav a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -0.35rem;
  width: 100%;
  height: 2px;
  border-radius: 999px;
  background: var(--primary);
  transform: scaleX(0);
  transform-origin: center;
  transition: transform var(--trans);
}

.site-nav a:hover,
.site-nav a:focus-visible {
  color: var(--primary);
}

.site-nav a:hover::after,
.site-nav a:focus-visible::after {
  transform: scaleX(1);
}

.mobile-toggle {
  padding: 0.5rem;
  margin-right: -0.5rem;
  border-radius: 999px;
  border: 1px solid transparent;
  background: rgba(255, 255, 255, 0.7);
}

.mobile-menu-overlay {
  background: rgba(248, 250, 252, 0.94);
}

.mobile-nav-links a {
  font-size: clamp(1.35rem, 5vw, 2rem);
  font-weight: 700;
  text-align: center;
}

.hero {
  padding-top: clamp(3rem, 6vw, 5rem);
  padding-bottom: clamp(4rem, 8vw, 6rem);
}

.hero-grid {
  gap: clamp(2rem, 5vw, 4rem);
}

.hero-copy {
  max-width: 40rem;
}

.hero h1 {
  font-size: clamp(2.8rem, 5vw, 5rem);
}

.hero-text {
  font-size: 1.08rem;
  max-width: 34rem;
  color: var(--text-muted);
}

.hero-actions {
  gap: 0.85rem;
  flex-wrap: wrap;
}

.hero-trust {
  gap: 0.75rem;
}

.trust-pill,
.hero-logos span {
  border-radius: 999px;
  box-shadow: var(--shadow-sm);
}

.trust-pill {
  background: rgba(255, 255, 255, 0.75);
}

.hero-logos span {
  background: rgba(255, 255, 255, 0.88);
  border: 1px solid var(--border);
  color: var(--text-muted);
}

.dashboard-shell {
  border-radius: 24px;
  background: rgba(255, 255, 255, 0.94);
  box-shadow: var(--shadow-lg);
}

.dashboard-topbar {
  align-items: center;
}

.topbar-title {
  font-size: 0.9rem;
  font-weight: 700;
  color: var(--text-muted);
}

.topbar-dots span {
  background: #cbd5e1;
}

.dashboard-body {
  grid-template-columns: 110px 1fr;
}

.dashboard-sidebar {
  display: grid;
  gap: 0.5rem;
}

.sidebar-item {
  font-size: 0.8rem;
  padding: 0.5rem 0.7rem;
  border-radius: 0.75rem;
  color: var(--text-muted);
}

.sidebar-item.active {
  background: var(--surface-alt);
  color: var(--text);
}

.mini-label {
  font-size: 0.78rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--accent);
  margin-bottom: 0.25rem;
}

.dashboard-heading {
  gap: 1rem;
  align-items: flex-start;
}

.status-pill {
  font-size: 0.8rem;
  background: #dcfce7;
  color: #166534;
  padding: 0.35rem 0.7rem;
  white-space: nowrap;
}

.dashboard-card {
  border-radius: 1rem;
  background: rgba(255,255,255,0.9);
  min-height: 5.5rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  box-shadow: var(--shadow-sm);
}

.dashboard-card.secondary {
  background: var(--surface-soft);
}

.card-label {
  letter-spacing: 0.08em;
}

.chart-bars span {
  background: linear-gradient(180deg, var(--accent), var(--primary));
  border-radius: 999px 999px 0 0;
}

.dashboard-card ul {
  margin: 0.4rem 0 0;
  padding-left: 1rem;
  color: var(--text-muted);
  font-weight: 600;
}

.floating-pill {
  padding: 0.7rem 1rem;
  background: rgba(255, 255, 255, 0.96);
  box-shadow: var(--shadow-sm);
}

.floating-pill.one {
  top: -18px;
  right: 16px;
}

.floating-pill.two {
  bottom: -18px;
  left: -16px;
}

.marquee-section {
  background: #fafafa;
}

.marquee-item {
  font-size: 1rem;
  font-weight: 800;
  color: var(--text-muted);
  opacity: 0.78;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.bento-card {
  border-radius: 24px;
  background: rgba(255, 255, 255, 0.9);
  box-shadow: var(--shadow-sm);
}

.bento-card:hover {
  border-color: rgba(37, 99, 235, 0.28);
  box-shadow: var(--shadow-md);
}

.bento-primary {
  background: linear-gradient(180deg, rgba(37, 99, 235, 0.06), rgba(255, 255, 255, 0.9));
  border-color: rgba(37, 99, 235, 0.18);
}

.link-cta {
  color: var(--accent);
  font-weight: 700;
}

.trust-metrics {
  gap: var(--space-3);
}

.metric-item {
  border: 1px solid var(--border);
  padding: var(--space-3);
  border-radius: 1rem;
  background: rgba(255,255,255,0.88);
  box-shadow: var(--shadow-sm);
}

.metric-val {
  font-size: clamp(2rem, 4vw, 3rem);
  font-weight: 800;
}

.metric-label {
  font-size: 0.92rem;
  font-weight: 600;
  color: var(--text-muted);
}

.work-info {
  max-width: 34rem;
}

.tech-badges span,
.tech-tags span {
  border-radius: 999px;
}

.work-visual-mockup {
  min-height: 20rem;
  border-radius: 24px;
  background: linear-gradient(180deg, rgba(15, 23, 42, 0.04), rgba(37, 99, 235, 0.04));
  box-shadow: var(--shadow-sm);
}

.process-step {
  border-radius: 24px;
  background: rgba(255,255,255,0.9);
  box-shadow: var(--shadow-sm);
}

.step-num {
  color: var(--accent);
  font-weight: 800;
}

.tech-tags span {
  background: rgba(255,255,255,0.9);
  border: 1px solid var(--border);
}

.testimonial-box {
  border-radius: 24px;
  background: rgba(255,255,255,0.92);
  box-shadow: var(--shadow-sm);
}

.quote {
  font-weight: 600;
}

.cta-form-container {
  border-radius: 28px;
  box-shadow: var(--shadow-lg);
}

.cta-form input,
.cta-form textarea {
  border: 1px solid var(--border);
  border-radius: 16px;
}

.cta-form input:focus,
.cta-form textarea:focus {
  border-color: rgba(37, 99, 235, 0.6);
  box-shadow: 0 0 0 4px rgba(37, 99, 235, 0.12);
}

.site-footer {
  background: rgba(15, 23, 42, 0.96);
  color: rgba(255,255,255,0.78);
  border-top: 1px solid rgba(255,255,255,0.08);
}

.site-footer .brand,
.site-footer h4,
.site-footer a,
.site-footer p {
  color: inherit;
}

.site-footer .brand span {
  color: #93c5fd;
}

.footer-links a,
.footer-legal a {
  font-weight: 600;
}

.footer-links a:hover,
.footer-links a:focus-visible,
.footer-legal a:hover,
.footer-legal a:focus-visible {
  color: #fff;
}

.newsletter input {
  border: 1px solid rgba(255,255,255,0.12);
  background: rgba(255,255,255,0.08);
  color: #fff;
}

.newsletter input::placeholder {
  color: rgba(255,255,255,0.5);
}

@media (max-width: 992px) {
  .site-nav {
    gap: 1rem;
  }

  .header-actions {
    gap: 0.5rem;
  }

  .nav-cta {
    padding-inline: 1rem;
  }

  .hero-copy,
  .work-info,
  .cta-copy {
    max-width: none;
  }

  .dashboard-body {
    grid-template-columns: 1fr;
  }

  .dashboard-sidebar {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }

  .floating-pill.two {
    left: 12px;
  }
}

@media (max-width: 640px) {
  .topbar-inner {
    gap: 0.75rem;
  }

  .hero {
    padding-top: 2.5rem;
  }

  .hero h1 {
    font-size: clamp(2.25rem, 11vw, 3.25rem);
  }

  .hero-actions {
    flex-direction: column;
    align-items: stretch;
  }

  .dashboard-grid,
  .trust-metrics,
  .testimonial-grid,
  .tech-ecosystem,
  .footer-layout,
  .cta-grid,
  .work-row,
  .work-row.reverse {
    grid-template-columns: 1fr;
  }

  .work-results {
    gap: 0.75rem;
  }

  .cta-form-container {
    padding: 1.25rem;
  }

  .newsletter {
    flex-direction: column;
  }

  .newsletter .btn-primary {
    width: 100%;
  }
}
</style>
