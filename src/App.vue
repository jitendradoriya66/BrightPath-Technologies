<template>
  <div class="app-shell">
    <a class="skip-link" href="#main">Skip to content</a>

    <header class="topbar" :class="{ scrolled: isScrolled }">
      <div class="container topbar-inner">
        <a class="brand" href="#">BrightPath<span>Studio</span></a>
        <nav class="site-nav" aria-label="Primary navigation">
          <a href="#services">Services</a>
          <a href="#work">Work</a>
          <a href="#process">Process</a>
          <a href="#contact">Contact</a>
        </nav>
        <a class="btn btn-primary nav-cta" href="#contact">Book a call</a>
        <button class="mobile-toggle" @click="toggleMobileMenu" :aria-expanded="mobileMenuOpen.toString()" aria-controls="mobile-menu" aria-label="Toggle navigation">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <path d="M4 6h16M4 12h16M4 18h16" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
          </svg>
        </button>
      </div>
      <div v-if="mobileMenuOpen" id="mobile-menu" class="mobile-nav">
        <div class="container mobile-nav-links">
          <a href="#services" @click="mobileMenuOpen = false">Services</a>
          <a href="#work" @click="mobileMenuOpen = false">Work</a>
          <a href="#process" @click="mobileMenuOpen = false">Process</a>
          <a href="#contact" @click="mobileMenuOpen = false">Contact</a>
        </div>
      </div>
    </header>

    <main id="main">
      <section class="hero section" aria-labelledby="hero-heading">
        <div class="container hero-grid">
          <div class="hero-copy reveal">
            <p class="eyebrow">Premium software for ambitious teams</p>
            <h1 id="hero-heading">We build software that feels as expensive as the product behind it.</h1>
            <p class="hero-text">From product strategy to launch-ready engineering, we create polished digital experiences that help companies win faster and feel unmistakably premium.</p>
            <div class="hero-actions">
              <a class="btn btn-primary" href="#contact">Start your project <span aria-hidden="true">↗</span></a>
              <a class="btn btn-secondary" href="#services">Explore capabilities</a>
            </div>
            <div class="hero-badges" aria-label="Focus areas">
              <span>Product strategy</span>
              <span>Custom engineering</span>
              <span>Launch support</span>
            </div>
          </div>

          <div class="hero-visual reveal" aria-hidden="true">
            <div class="hero-orb orb-one"></div>
            <div class="hero-orb orb-two"></div>
            <div class="surface-card main-card">
              <div class="card-top">
                <span class="chip chip-primary">Live product</span>
                <span class="chip">Q3 launch</span>
              </div>
              <div class="main-graph">
                <div class="graph-line"></div>
                <div class="graph-line short"></div>
                <div class="graph-line"></div>
              </div>
              <div class="card-metrics">
                <div>
                  <strong>+318%</strong>
                  <span>engagement</span>
                </div>
                <div>
                  <strong>98%</strong>
                  <span>uptime</span>
                </div>
              </div>
            </div>
            <div class="surface-card floating-card one">
              <p class="mini-label">AI orchestration</p>
              <strong>Adaptive workflows</strong>
            </div>
            <div class="surface-card floating-card two">
              <p class="mini-label">Revenue</p>
              <strong>$4.2M pipeline</strong>
            </div>
            <div class="surface-card floating-card three">
              <p class="mini-label">Team</p>
              <strong>12 specialists online</strong>
            </div>
          </div>
        </div>
      </section>

      <section class="logo-strip reveal">
        <div class="container logo-strip-inner">
          <p>Trusted by founders building the next category</p>
          <div class="logo-row">
            <span v-for="logo in logos" :key="logo">{{ logo }}</span>
          </div>
        </div>
      </section>

      <section id="services" class="section reveal">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Capabilities</p>
            <h2>Designed for companies that want more than a polished landing page.</h2>
            <p>We blend strategy, product design, and engineering into a process that feels clear, fast, and deeply intentional.</p>
          </div>
          <div class="service-grid">
            <article v-for="service in services" :key="service.title" class="service-card" :class="service.featured ? 'featured' : ''">
              <div class="service-icon" :style="{ background: service.gradient }">{{ service.icon }}</div>
              <h3>{{ service.title }}</h3>
              <p>{{ service.description }}</p>
              <a href="#contact">Learn more</a>
            </article>
          </div>
        </div>
      </section>

      <section class="section reveal">
        <div class="container metrics-panel">
          <div v-for="stat in stats" :key="stat.label" class="metric-tile">
            <strong>{{ stat.value }}</strong>
            <span>{{ stat.label }}</span>
          </div>
        </div>
      </section>

      <section id="work" class="section reveal">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Selected work</p>
            <h2>Product launches engineered to feel effortless and premium.</h2>
          </div>
          <div class="work-grid">
            <article class="work-card work-card-large">
              <div class="work-visual">
                <div class="browser-frame">
                  <div class="browser-bar"><span></span><span></span><span></span></div>
                  <div class="browser-body">
                    <div class="browser-panel large"></div>
                    <div class="browser-panel"></div>
                    <div class="browser-panel"></div>
                  </div>
                </div>
              </div>
              <div class="work-copy">
                <p class="mini-label">Fintech platform</p>
                <h3>Global payment intelligence for a modern operations team.</h3>
                <p>We rebuilt a legacy experience into a sharper, more modular product that made transaction insight feel immediate and trustworthy.</p>
                <div class="metric-row">
                  <span>+300%</span>
                  <span>+42% conversion</span>
                  <span>98% retention</span>
                </div>
              </div>
            </article>
            <article class="work-card">
              <div class="work-copy">
                <p class="mini-label">SaaS product</p>
                <h3>AI workspace with onboarding that feels effortless from the first click.</h3>
                <p>We paired interaction design with reliable engineering to ship a product that felt premium from day one.</p>
              </div>
            </article>
          </div>
        </div>
      </section>

      <section id="process" class="section section-soft reveal">
        <div class="container">
          <div class="section-heading">
            <p class="eyebrow">Process</p>
            <h2>A calm, decisive path from idea to launch.</h2>
          </div>
          <div class="timeline">
            <div v-for="step in process" :key="step.title" class="timeline-step">
              <div class="step-badge">0{{ step.index }}</div>
              <h3>{{ step.title }}</h3>
              <p>{{ step.description }}</p>
            </div>
          </div>
        </div>
      </section>

      <section class="section reveal">
        <div class="container testimonial-section">
          <div class="testimonial-intro">
            <p class="eyebrow">Testimonials</p>
            <h2>Trusted by founders who care deeply about quality.</h2>
            <p>Every engagement is shaped around speed, clarity, and a product that feels unmistakably polished.</p>
          </div>
          <div class="testimonial-track">
            <article v-for="testimonial in testimonials" :key="testimonial.name" class="testimonial-card">
              <div class="rating">★★★★★</div>
              <p>“{{ testimonial.quote }}”</p>
              <div class="person">
                <strong>{{ testimonial.name }}</strong>
                <span>{{ testimonial.role }}</span>
              </div>
            </article>
          </div>
        </div>
      </section>

      <section id="contact" class="section reveal">
        <div class="container contact-shell">
          <div class="contact-copy">
            <p class="eyebrow">Let’s build something exceptional</p>
            <h2>Bring us your boldest idea and we’ll shape it into a product people remember.</h2>
            <p>Whether you need a new platform, a thoughtful redesign, or a refined AI experience, we’ll help you move fast with clarity.</p>
            <ul>
              <li>Rapid discovery and product framing</li>
              <li>Design-led engineering from day one</li>
              <li>Reliable delivery with premium polish</li>
            </ul>
          </div>
          <form class="contact-form" @submit.prevent="submitForm">
            <div class="form-group">
              <label for="name">Name</label>
              <input ref="nameInput" id="name" type="text" required />
            </div>
            <div class="form-group">
              <label for="email">Work email</label>
              <input ref="emailInput" id="email" type="email" required />
            </div>
            <div class="form-group">
              <label for="message">What are you building?</label>
              <textarea ref="messageInput" id="message" rows="4" required></textarea>
            </div>
            <button type="submit" class="btn btn-primary">Request consultation</button>
          </form>
        </div>
      </section>
    </main>

    <footer class="footer">
      <div class="container footer-grid">
        <div>
          <a class="brand footer-brand" href="#">BrightPath</a>
          <p>High-end software design and development for ambitious product teams.</p>
        </div>
        <div>
          <h3>Explore</h3>
          <a href="#services">Services</a>
          <a href="#work">Selected work</a>
          <a href="#process">Process</a>
        </div>
        <div>
          <h3>Contact</h3>
          <a href="#contact">Book a call</a>
          <a href="#contact">hello@brightpath.dev</a>
          <a href="#contact">+1 (555) 014-2030</a>
        </div>
        <div>
          <h3>Follow</h3>
          <a href="#">LinkedIn</a>
          <a href="#">X</a>
          <a href="#">Dribbble</a>
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
      logos: ['Nova Labs', 'Northstar', 'Aurelia', 'Helio', 'Lattice'],
      services: [
        {
          title: 'Product strategy',
          description: 'Experience design, positioning, and roadmap framing that makes the product feel inevitable.',
          icon: '✦',
          gradient: 'linear-gradient(135deg, #6D28D9, #7C3AED)',
          featured: true
        },
        {
          title: 'AI experiences',
          description: 'Workflow design and intelligent interfaces that feel calm, useful, and deeply crafted.',
          icon: '◌',
          gradient: 'linear-gradient(135deg, #06B6D4, #2563eb)'
        },
        {
          title: 'Custom product engineering',
          description: 'Reliable frontends and robust systems built for rapid iteration and long-term scale.',
          icon: '⬢',
          gradient: 'linear-gradient(135deg, #FF6B35, #F59E0B)'
        },
        {
          title: 'Launch enablement',
          description: 'Rollout support, analytics, and growth systems that keep momentum going after launch.',
          icon: '↗',
          gradient: 'linear-gradient(135deg, #10B981, #34D399)',
          featured: true
        }
      ],
      stats: [
        { value: '12+', label: 'launches delivered this year' },
        { value: '4.9/5', label: 'client satisfaction score' },
        { value: '98%', label: 'retention across milestone releases' },
        { value: '24h', label: 'average response time' }
      ],
      process: [
        { index: 1, title: 'Discover', description: 'We define the opportunity and shape the product experience around what matters most.' },
        { index: 2, title: 'Design', description: 'We turn strategy into elegant interaction patterns and a clear product narrative.' },
        { index: 3, title: 'Build', description: 'We engineer the experience with speed, reliability, and careful quality bar.' },
        { index: 4, title: 'Scale', description: 'We refine analytics, rollout, and iteration loops so the product keeps winning.' }
      ],
      testimonials: [
        {
          name: 'Mara Chen',
          role: 'Founder, Oriel AI',
          quote: 'The experience felt unmistakably premium from the first presentation through launch. Every detail was considered.'
        },
        {
          name: 'Alex Rivera',
          role: 'VP Product, Northstar Labs',
          quote: 'They translated a complex product vision into something beautiful, intuitive, and ready for real users.'
        }
      ]
    }
  },
  mounted() {
    this.observeReveal()
    this.handleScroll()
    window.addEventListener('scroll', this.handleScroll)
    window.addEventListener('resize', this.handleResize)
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll)
    window.removeEventListener('resize', this.handleResize)
    if (this.revealObserver) {
      this.revealObserver.disconnect()
    }
  },
  methods: {
    toggleMobileMenu() {
      this.mobileMenuOpen = !this.mobileMenuOpen
    },
    handleScroll() {
      this.isScrolled = window.scrollY > 12
    },
    handleResize() {
      if (window.innerWidth > 768) {
        this.mobileMenuOpen = false
      }
    },
    observeReveal() {
      if (typeof window === 'undefined' || !('IntersectionObserver' in window)) {
        document.querySelectorAll('.reveal').forEach((item) => item.classList.add('visible'))
        return
      }
      this.revealObserver = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible')
            this.revealObserver.unobserve(entry.target)
          }
        })
      }, { threshold: 0.16 })
      document.querySelectorAll('.reveal').forEach((item) => {
        this.revealObserver.observe(item)
      })
    },
    submitForm() {
      const name = this.$refs.nameInput.value.trim()
      const email = this.$refs.emailInput.value.trim()
      const message = this.$refs.messageInput.value.trim()
      if (!name || !email || !message) {
        alert('Please complete all fields before submitting.')
        return
      }
      alert('Thanks for reaching out. We will contact you within one business day.')
      this.$refs.nameInput.value = ''
      this.$refs.emailInput.value = ''
      this.$refs.messageInput.value = ''
    }
  }
}
</script>

<style scoped>
.app-shell {
  min-height: 100vh;
  background: linear-gradient(180deg, #f8fafc 0%, #f3f7ff 100%);
  color: var(--text);
  overflow-x: hidden;
}

.container {
  width: min(100%, 1320px);
  margin: 0 auto;
  padding: 0 1.4rem;
}

.section {
  padding: 6.4rem 0;
}

.section-soft {
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.94), rgba(244, 248, 255, 0.96));
  border-block: 1px solid rgba(15, 23, 42, 0.06);
}

.skip-link {
  position: absolute;
  left: 1rem;
  top: -3.5rem;
  z-index: 300;
  padding: 0.8rem 1rem;
  border-radius: 999px;
  background: var(--primary);
  color: #fff;
}

.skip-link:focus {
  top: 1rem;
}

.topbar {
  position: sticky;
  top: 0;
  z-index: 200;
  padding: 1rem 0;
  background: rgba(248, 250, 252, 0.76);
  backdrop-filter: blur(20px);
  border-bottom: 1px solid rgba(15, 23, 42, 0.06);
}

.topbar.scrolled {
  box-shadow: 0 12px 28px rgba(15, 23, 42, 0.06);
}

.topbar-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
}

.brand {
  font-size: 1rem;
  font-weight: 800;
  letter-spacing: -0.03em;
  color: var(--text);
}

.brand span {
  color: var(--primary);
}

.site-nav {
  display: flex;
  gap: 1.25rem;
}

.site-nav a,
.mobile-nav-links a {
  font-size: 0.95rem;
  color: var(--text-muted);
  transition: var(--trans);
}

.site-nav a:hover,
.mobile-nav-links a:hover,
.site-nav a:focus-visible,
.mobile-nav-links a:focus-visible {
  color: var(--primary);
}

.nav-cta {
  padding: 0.82rem 1rem;
}

.mobile-toggle {
  display: none;
  align-items: center;
  justify-content: center;
  width: 2.8rem;
  height: 2.8rem;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: var(--surface);
  color: var(--text);
}

.mobile-nav {
  background: rgba(255, 255, 255, 0.95);
  border-top: 1px solid var(--border);
}

.mobile-nav-links {
  display: flex;
  flex-direction: column;
  gap: 0.85rem;
  padding: 1rem 0 1.2rem;
}

.hero {
  padding-top: 5.4rem;
  padding-bottom: 4.4rem;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.02fr 0.98fr;
  gap: 3rem;
  align-items: center;
}

.eyebrow {
  display: inline-flex;
  margin-bottom: 1rem;
  text-transform: uppercase;
  letter-spacing: 0.24em;
  font-size: 0.76rem;
  font-weight: 700;
  color: var(--primary);
}

.hero h1 {
  font-size: clamp(2.8rem, 5vw, 4.8rem);
  line-height: 0.95;
  letter-spacing: -0.045em;
  margin-bottom: 1.3rem;
  max-width: 760px;
}

.hero-text {
  font-size: 1.12rem;
  line-height: 1.8;
  color: var(--text-muted);
  max-width: 660px;
  margin-bottom: 1.8rem;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 0.95rem;
  margin-bottom: 1.5rem;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.6rem;
  border-radius: 999px;
  font-weight: 700;
  border: 1px solid transparent;
  transition: var(--trans);
  text-decoration: none;
}

.btn:hover {
  transform: translateY(-2px);
}

.btn-primary {
  padding: 0.95rem 1.2rem;
  background: linear-gradient(135deg, var(--primary), var(--primary-strong));
  color: white;
  box-shadow: 0 16px 32px rgba(109, 40, 217, 0.22);
}

.btn-secondary {
  padding: 0.95rem 1.2rem;
  background: rgba(255, 255, 255, 0.9);
  color: var(--text);
  border-color: var(--border);
}

.hero-badges {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
}

.hero-badges span {
  display: inline-flex;
  align-items: center;
  padding: 0.55rem 0.8rem;
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.82);
  border: 1px solid var(--border);
  color: var(--text);
  font-size: 0.9rem;
  font-weight: 600;
}

.hero-visual {
  position: relative;
  min-height: 560px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero-visual::before,
.hero-visual::after {
  content: '';
  position: absolute;
  inset: 0;
  border-radius: 2rem;
  pointer-events: none;
}

.hero-visual::before {
  background: radial-gradient(circle at top left, rgba(109, 40, 217, 0.16), transparent 45%), radial-gradient(circle at bottom right, rgba(255, 107, 53, 0.14), transparent 38%);
}

.hero-visual::after {
  background-image: linear-gradient(rgba(15, 23, 42, 0.03) 1px, transparent 1px), linear-gradient(90deg, rgba(15, 23, 42, 0.03) 1px, transparent 1px);
  background-size: 28px 28px;
  mask-image: linear-gradient(180deg, rgba(0, 0, 0, 0.6), transparent 100%);
}

.surface-card {
  position: absolute;
  border: 1px solid rgba(15, 23, 42, 0.08);
  background: rgba(255, 255, 255, 0.86);
  backdrop-filter: blur(24px);
  box-shadow: 0 22px 48px rgba(15, 23, 42, 0.12);
  border-radius: 1.5rem;
}

.main-card {
  width: min(100%, 450px);
  padding: 1.15rem;
  z-index: 2;
  transform: rotate(-2deg);
}

.card-top {
  display: flex;
  justify-content: space-between;
  gap: 0.6rem;
  margin-bottom: 1rem;
}

.chip {
  display: inline-flex;
  padding: 0.4rem 0.7rem;
  border-radius: 999px;
  background: rgba(15, 23, 42, 0.05);
  color: var(--text-muted);
  font-size: 0.78rem;
  font-weight: 700;
}

.chip-primary {
  background: rgba(109, 40, 217, 0.12);
  color: var(--primary);
}

.main-graph {
  border-radius: 1.2rem;
  background: linear-gradient(135deg, rgba(109, 40, 217, 0.12), rgba(6, 182, 212, 0.16));
  padding: 1rem;
  display: grid;
  gap: 0.7rem;
  min-height: 220px;
}

.graph-line {
  height: 16px;
  border-radius: 999px;
  background: linear-gradient(90deg, var(--primary), var(--accent));
}

.graph-line.short {
  width: 72%;
}

.card-metrics {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 0.8rem;
  margin-top: 1rem;
}

.card-metrics div {
  padding: 0.9rem;
  border-radius: 1rem;
  background: #fff;
  border: 1px solid rgba(15, 23, 42, 0.06);
}

.card-metrics strong {
  display: block;
  font-size: 1.1rem;
  color: var(--text);
}

.card-metrics span {
  color: var(--text-muted);
  font-size: 0.84rem;
}

.floating-card {
  padding: 0.95rem 1rem;
  z-index: 3;
  animation: bob 5s ease-in-out infinite;
}

.floating-card.one {
  top: 3.2rem;
  right: 0.8rem;
}

.floating-card.two {
  bottom: 2rem;
  right: 0.6rem;
  animation-delay: 1s;
}

.floating-card.three {
  bottom: 4rem;
  left: 0.3rem;
  animation-delay: 1.8s;
}

.mini-label {
  font-size: 0.72rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.2em;
  color: var(--primary);
  margin-bottom: 0.3rem;
}

.logo-strip {
  padding-top: 0;
  padding-bottom: 2rem;
}

.logo-strip-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  padding: 1rem 1.3rem;
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.76);
  border: 1px solid var(--border);
}

.logo-strip-inner p {
  color: var(--text-muted);
  font-size: 0.95rem;
}

.logo-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.7rem;
}

.logo-row span {
  padding: 0.5rem 0.8rem;
  border-radius: 999px;
  background: rgba(15, 23, 42, 0.04);
  color: var(--text);
  font-weight: 700;
}

.section-heading {
  max-width: 760px;
  margin-bottom: 2.2rem;
}

.section-heading h2 {
  font-size: clamp(1.8rem, 3vw, 2.45rem);
  margin-bottom: 0.75rem;
  letter-spacing: -0.03em;
}

.section-heading p {
  color: var(--text-muted);
  line-height: 1.8;
}

.service-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1.1rem;
}

.service-card {
  position: relative;
  overflow: hidden;
  padding: 1.45rem;
  border-radius: 1.45rem;
  border: 1px solid var(--border);
  background: linear-gradient(180deg, rgba(255,255,255,0.96), rgba(248,250,252,0.96));
  box-shadow: 0 10px 24px rgba(15, 23, 42, 0.04);
  transition: var(--trans);
}

.service-card::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(255,255,255,0.95), rgba(255,255,255,0));
  pointer-events: none;
}

.service-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 24px 40px rgba(109, 40, 217, 0.16);
}

.service-card.featured {
  grid-column: span 2;
}

.service-icon {
  width: 3.2rem;
  height: 3.2rem;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 1.1rem;
  color: #fff;
  font-size: 1.15rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.service-card h3 {
  font-size: 1.22rem;
  margin-bottom: 0.7rem;
}

.service-card p {
  color: var(--text-muted);
  line-height: 1.75;
  margin-bottom: 1rem;
}

.service-card a {
  color: var(--primary);
  font-weight: 700;
}

.metrics-panel {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 1rem;
}

.metric-tile {
  padding: 1.5rem;
  border-radius: 1.3rem;
  background: rgba(255, 255, 255, 0.9);
  border: 1px solid var(--border);
  box-shadow: 0 10px 24px rgba(15, 23, 42, 0.04);
}

.metric-tile strong {
  display: block;
  font-size: 1.55rem;
  color: var(--text);
  margin-bottom: 0.3rem;
}

.metric-tile span {
  color: var(--text-muted);
  font-size: 0.95rem;
}

.work-grid {
  display: grid;
  gap: 1.1rem;
}

.work-card {
  border-radius: 1.55rem;
  padding: 1.35rem;
  background: rgba(255, 255, 255, 0.93);
  border: 1px solid var(--border);
  box-shadow: 0 12px 30px rgba(15, 23, 42, 0.04);
}

.work-card-large {
  display: grid;
  grid-template-columns: 1.05fr 0.95fr;
  gap: 1.2rem;
  align-items: center;
}

.work-visual {
  border-radius: 1.25rem;
  padding: 1rem;
  background: linear-gradient(135deg, rgba(109, 40, 217, 0.12), rgba(6, 182, 212, 0.12));
  min-height: 280px;
}

.browser-frame {
  border: 1px solid rgba(15, 23, 42, 0.08);
  border-radius: 1rem;
  background: #fff;
  overflow: hidden;
}

.browser-bar {
  height: 12px;
  background: rgba(15, 23, 42, 0.05);
  display: flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0 0.8rem;
}

.browser-bar span {
  display: inline-block;
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: rgba(15, 23, 42, 0.2);
}

.browser-body {
  padding: 1rem;
  display: grid;
  gap: 0.7rem;
}

.browser-panel {
  height: 54px;
  border-radius: 0.8rem;
  background: linear-gradient(90deg, var(--primary), rgba(109, 40, 217, 0.2));
}

.browser-panel.large {
  height: 90px;
  background: linear-gradient(90deg, var(--accent), rgba(255, 107, 53, 0.18));
}

.work-copy h3 {
  font-size: 1.3rem;
  margin-bottom: 0.75rem;
  letter-spacing: -0.02em;
}

.work-copy p {
  color: var(--text-muted);
  line-height: 1.75;
}

.metric-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.65rem;
  margin-top: 1rem;
}

.metric-row span {
  padding: 0.45rem 0.7rem;
  border-radius: 999px;
  background: rgba(109, 40, 217, 0.08);
  color: var(--primary);
  font-weight: 700;
  font-size: 0.9rem;
}

.timeline {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 1rem;
}

.timeline-step {
  padding: 1.2rem;
  border-radius: 1.2rem;
  background: rgba(255, 255, 255, 0.92);
  border: 1px solid var(--border);
  box-shadow: 0 10px 24px rgba(15, 23, 42, 0.04);
}

.timeline-step h3 {
  margin-bottom: 0.55rem;
}

.timeline-step p {
  color: var(--text-muted);
  line-height: 1.75;
}

.step-badge {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 2.2rem;
  height: 2.2rem;
  border-radius: 999px;
  background: linear-gradient(135deg, var(--primary), var(--accent));
  color: #fff;
  font-size: 0.9rem;
  font-weight: 700;
  margin-bottom: 0.85rem;
}

.testimonial-section {
  display: grid;
  grid-template-columns: 0.88fr 1.12fr;
  gap: 1.2rem;
  align-items: start;
}

.testimonial-intro h2 {
  font-size: clamp(1.8rem, 3vw, 2.35rem);
  margin-bottom: 0.75rem;
  letter-spacing: -0.03em;
}

.testimonial-intro p {
  color: var(--text-muted);
  line-height: 1.8;
}

.testimonial-track {
  display: grid;
  gap: 0.9rem;
}

.testimonial-card {
  padding: 1.2rem;
  border-radius: 1.2rem;
  background: linear-gradient(135deg, rgba(255,255,255,0.96), rgba(244,247,255,0.96));
  border: 1px solid var(--border);
  box-shadow: 0 12px 24px rgba(15, 23, 42, 0.04);
}

.rating {
  color: var(--accent);
  letter-spacing: 0.24em;
  font-size: 0.9rem;
  margin-bottom: 0.8rem;
}

.testimonial-card p {
  color: var(--text-muted);
  line-height: 1.76;
  margin-bottom: 0.9rem;
}

.person {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
}

.person span {
  color: var(--text-muted);
  font-size: 0.9rem;
}

.contact-shell {
  display: grid;
  grid-template-columns: 0.95fr 1.05fr;
  gap: 1.3rem;
  align-items: start;
}

.contact-copy {
  padding: 1.2rem 0;
}

.contact-copy h2 {
  font-size: clamp(1.8rem, 3vw, 2.35rem);
  margin-bottom: 0.75rem;
  letter-spacing: -0.03em;
}

.contact-copy p,
.contact-copy li {
  color: var(--text-muted);
  line-height: 1.8;
}

.contact-copy ul {
  display: grid;
  gap: 0.7rem;
  padding-left: 1rem;
  margin-top: 1rem;
}

.contact-form {
  padding: 1.25rem;
  border-radius: 1.4rem;
  background: rgba(255, 255, 255, 0.94);
  border: 1px solid var(--border);
  box-shadow: 0 16px 32px rgba(15, 23, 42, 0.08);
}

.form-group {
  margin-bottom: 0.95rem;
}

.form-group label {
  display: block;
  margin-bottom: 0.45rem;
  font-weight: 700;
  color: var(--text);
}

.form-group input,
.form-group textarea {
  width: 100%;
  border: 1px solid var(--border);
  border-radius: 0.95rem;
  padding: 0.85rem 0.95rem;
  background: #fff;
  color: var(--text);
  font: inherit;
  transition: var(--trans);
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--primary);
  box-shadow: 0 0 0 4px rgba(109, 40, 217, 0.12);
}

.footer {
  padding: 3rem 0 2.6rem;
  background: linear-gradient(135deg, rgba(15, 23, 42, 0.97), rgba(30, 41, 59, 0.99));
  color: rgba(248, 250, 252, 0.75);
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr 0.8fr 0.8fr;
  gap: 1rem;
}

.footer-brand {
  display: inline-flex;
  margin-bottom: 0.7rem;
  color: #fff;
}

.footer h3 {
  color: #fff;
  font-size: 0.95rem;
  margin-bottom: 0.7rem;
}

.footer a {
  display: block;
  color: rgba(248, 250, 252, 0.74);
  margin-bottom: 0.45rem;
  transition: var(--trans);
}

.footer a:hover {
  color: #fff;
}

.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 700ms ease, transform 700ms ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

@keyframes bob {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

@media (max-width: 960px) {
  .hero-grid,
  .testimonial-section,
  .contact-shell,
  .work-card-large {
    grid-template-columns: 1fr;
  }

  .hero-visual {
    min-height: 460px;
  }

  .timeline {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 768px) {
  .site-nav,
  .nav-cta {
    display: none;
  }

  .mobile-toggle {
    display: inline-flex;
  }

  .section {
    padding: 4.4rem 0;
  }

  .service-grid,
  .metrics-panel,
  .timeline {
    grid-template-columns: 1fr;
  }

  .service-card.featured {
    grid-column: span 1;
  }

  .logo-strip-inner {
    flex-direction: column;
    align-items: flex-start;
    border-radius: 1.2rem;
  }

  .footer-grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 560px) {
  .container {
    padding: 0 1rem;
  }

  .hero h1 {
    font-size: 2.55rem;
  }

  .hero-visual {
    min-height: 380px;
  }

  .main-card {
    width: 92%;
  }

  .floating-card.one {
    top: 1.6rem;
    right: 0.4rem;
  }

  .floating-card.two {
    bottom: 0.7rem;
    right: 0.2rem;
  }

  .floating-card.three {
    bottom: 2.4rem;
    left: 0;
  }

  .footer-grid {
    grid-template-columns: 1fr;
  }
}
</style>
