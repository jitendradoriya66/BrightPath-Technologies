<template>
  <div :data-theme="isDarkMode ? 'dark' : 'light'" class="app-wrapper">
    <!-- Spotlight Cursor Effect -->
    <div class="cursor-spotlight" :style="spotlightStyle"></div>

    <!-- 1. Announcement Bar -->
    <div class="announcement-bar">
      <div class="announcement-glow"></div>
      <span>✨ Now Launching BrightPath Agentic AI Sprints: Deploy custom LLM orchestration in 14 days.</span>
      <a href="#ai-solutions" class="learn-more-link">Explore Agents <i data-lucide="arrow-right"></i></a>
    </div>

    <!-- 2. Sticky Navigation -->
    <header class="navbar glass" :class="{ 'scrolled': isScrolled }">
      <div class="container nav-container">
        <a href="#" class="nav-logo">
          <div class="logo-wrapper">
            <img src="/logo.svg" alt="BrightPath Logo" class="logo-img animate-spin-slow" />
            <div class="logo-ring"></div>
          </div>
          <span class="logo-text">BrightPath</span>
        </a>

        <!-- Desktop Navigation Menu -->
        <nav class="nav-menu">
          <div class="nav-item">
            <a href="#services" class="nav-link">Services</a>
          </div>
          <div class="nav-item">
            <a href="#industries" class="nav-link">Industries</a>
          </div>
          <div class="nav-item">
            <a href="#process" class="nav-link">Process</a>
          </div>
          <div class="nav-item">
            <a href="#portfolio" class="nav-link">Work</a>
          </div>
          <div class="nav-item">
            <a href="#pricing" class="nav-link">Rates</a>
          </div>
          <div class="nav-item">
            <a href="#faq" class="nav-link">FAQ</a>
          </div>
          <div class="nav-item">
            <a href="#blog" class="nav-link">Journal</a>
          </div>
        </nav>

        <div class="nav-actions">
          <button @click="toggleTheme" class="theme-toggle-btn" aria-label="Toggle theme">
            <i :data-lucide="isDarkMode ? 'sun' : 'moon'"></i>
          </button>
          <a href="#contact" class="btn btn-primary nav-cta">Book Consultation</a>
          <button @click="isMobileMenuOpen = !isMobileMenuOpen" class="mobile-menu-toggle" aria-label="Toggle menu">
            <i :data-lucide="isMobileMenuOpen ? 'x' : 'menu'"></i>
          </button>
        </div>
      </div>

      <!-- Mobile Menu Dropdown -->
      <div v-if="isMobileMenuOpen" class="mobile-menu glass">
        <a href="#services" @click="isMobileMenuOpen = false">Services</a>
        <a href="#industries" @click="isMobileMenuOpen = false">Industries</a>
        <a href="#process" @click="isMobileMenuOpen = false">Process Blueprint</a>
        <a href="#portfolio" @click="isMobileMenuOpen = false">Case Studies</a>
        <a href="#pricing" @click="isMobileMenuOpen = false">Investment Plans</a>
        <a href="#faq" @click="isMobileMenuOpen = false">FAQ</a>
        <a href="#blog" @click="isMobileMenuOpen = false">Journal</a>
        <a href="#contact" class="btn btn-primary" @click="isMobileMenuOpen = false">Book Consultation</a>
      </div>
    </header>

    <!-- 3. Hero Section (Cinematic & Overloaded) -->
    <section class="hero-section" @mousemove="handleHeroMouseMove">
      <div class="hero-grid-background"></div>
      <div class="aurora-blobs">
        <div class="aurora-blob aurora-1"></div>
        <div class="aurora-blob aurora-2"></div>
        <div class="aurora-blob aurora-3"></div>
      </div>
      
      <div class="container hero-container">
        <div class="hero-content">
          <div class="badge badge-accent mb-4 hero-badge animate-float">
            <span>✨ System Integrator of the Year</span>
          </div>
          <h1 class="hero-title">
            We build <br />
            <span class="text-gradient">modern digital</span> <br />
            products.
          </h1>
          <p class="hero-subtitle">
            Engineered for startups, local market disruptors, and global scale enterprises. A premium software collective shifting ideas into high-performance web products.
          </p>
          
          <div class="hero-actions">
            <a href="#contact" class="btn btn-primary btn-lg shine-effect">Book Consultation</a>
            <a href="#portfolio" class="btn btn-secondary btn-lg">Explore Portfolio</a>
          </div>

          <!-- Live Metrics inside Hero -->
          <div class="hero-metrics">
            <div class="hero-metric-item">
              <span class="metric-num text-gradient-purple">240+</span>
              <span class="metric-lbl">Shipped globally</span>
            </div>
            <div class="hero-metric-item">
              <span class="hero-divider-dot"></span>
            </div>
            <div class="hero-metric-item">
              <span class="metric-num text-gradient-purple">99.9%</span>
              <span class="metric-lbl">Service Level Agreement</span>
            </div>
          </div>
        </div>

        <div class="hero-visual-wrapper">
          <!-- Glassmorphic Bento Frame -->
          <div class="hero-bento-glass glass" :style="heroVisualRotateStyle">
            <div class="bento-header">
              <div class="bento-dots"><span></span><span></span><span></span></div>
              <div class="bento-address">brightpath.core.ts</div>
            </div>
            <div class="bento-body">
              <div class="code-panel">
                <span class="code-line"><span class="keyword">import</span> { Agent } <span class="keyword">from</span> <span class="string">"@brightpath/ai"</span>;</span>
                <span class="code-line"><span class="keyword">const</span> app = <span class="keyword">new</span> DigitalProduct({</span>
                <span class="code-line">&nbsp;&nbsp;ux: <span class="string">"Apple-Level"</span>,</span>
                <span class="code-line">&nbsp;&nbsp;performance: <span class="string">"Stripe-Speed"</span></span>
                <span class="code-line">});</span>
                <span class="code-line">app.deploy({ latency: <span class="string">"<14ms"</span> });</span>
              </div>
              
              <!-- Live Dashboard preview element -->
              <div class="bento-stats-panel glass">
                <div class="bento-stats-header">
                  <span class="indicator-active"></span>
                  <span class="label">LIVE PERFORMANCE FEED</span>
                </div>
                <div class="bento-metric-row">
                  <div>
                    <span class="subtext">Daily Sessions</span>
                    <span class="num">192.4k</span>
                  </div>
                  <div>
                    <span class="subtext">Speed Index</span>
                    <span class="num text-gradient">0.4s</span>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Abstract floating tech tokens -->
          <div class="floating-tech-badges">
            <span class="tech-tag animate-float badge-1"><i data-lucide="cpu"></i> OpenAI</span>
            <span class="tech-tag animate-float badge-2"><i data-lucide="zap"></i> Edge Hydration</span>
            <span class="tech-tag animate-float badge-3"><i data-lucide="shield"></i> SSL Encrypted</span>
          </div>
        </div>
      </div>
    </section>

    <!-- 4. Trusted By Section -->
    <section class="trusted-by-section">
      <div class="container">
        <p class="trusted-title">BUILT FOR LEADING BRAND ECOSYSTEMS</p>
        <div class="logo-marquee-wrapper">
          <div class="logo-marquee">
            <span class="partner-logo">Vercel</span>
            <span class="partner-logo">Stripe</span>
            <span class="partner-logo">Linear</span>
            <span class="partner-logo">Framer</span>
            <span class="partner-logo">Supabase</span>
            <span class="partner-logo">Notion</span>
            <span class="partner-logo">GitHub</span>
            <!-- Duplicated -->
            <span class="partner-logo">Vercel</span>
            <span class="partner-logo">Stripe</span>
            <span class="partner-logo">Linear</span>
            <span class="partner-logo">Framer</span>
            <span class="partner-logo">Supabase</span>
            <span class="partner-logo">Notion</span>
            <span class="partner-logo">GitHub</span>
          </div>
        </div>
      </div>
    </section>

    <!-- 5. Bento Grid Company Statistics -->
    <section class="stats-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">Metrics</span>
          <h2>Numbers that demand attention</h2>
        </div>

        <div class="stats-bento-grid">
          <div class="stats-bento-card bento-large glass">
            <h3 class="bento-val text-gradient">240+</h3>
            <p class="bento-lbl">Scalable software systems constructed and maintained globally.</p>
            <div class="bento-graphic">
              <svg viewBox="0 0 200 100" class="mini-chart">
                <path d="M0,80 Q30,40 60,60 T120,20 T180,10 L200,10" fill="none" stroke="var(--primary)" stroke-width="4" stroke-linecap="round" />
              </svg>
            </div>
          </div>
          <div class="stats-bento-card glass">
            <h3 class="bento-val">99%</h3>
            <p class="bento-lbl">Client Retention & Satisfaction</p>
          </div>
          <div class="stats-bento-card glass">
            <h3 class="bento-val">18+</h3>
            <p class="bento-lbl">Global Countries Served</p>
          </div>
          <div class="stats-bento-card bento-wide glass">
            <h3 class="bento-val">8+ Years</h3>
            <p class="bento-lbl">Fostering digital evolution, modern UI architecture, and robust server deployments.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- 6. Services (Asymmetric layout) -->
    <section id="services" class="services-section">
      <div class="container">
        <div class="asymmetric-layout">
          <div class="asym-left">
            <span class="badge mb-2">Our Capabilities</span>
            <h2 class="section-title">An integrated engineering studio.</h2>
            <p class="section-desc text-muted">We eliminate organizational complexity by packaging elite product design, server management, AI modeling, and app deployment in one continuous engine.</p>
            
            <div class="interactive-service-preview glass mt-4">
              <span class="preview-title">Hover a card to investigate features</span>
              <div v-if="activeServiceIndex !== null" class="preview-content">
                <h4>{{ services[activeServiceIndex].title }}</h4>
                <ul class="preview-features">
                  <li v-for="feat in services[activeServiceIndex].features" :key="feat">
                    <i data-lucide="check-circle-2"></i> {{ feat }}
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <div class="asym-right">
            <div 
              v-for="(service, idx) in services" 
              :key="idx" 
              class="service-block-card glass"
              @mouseenter="activeServiceIndex = idx"
            >
              <div class="card-icon-box">
                <i :data-lucide="service.icon"></i>
              </div>
              <div class="card-text">
                <h3>{{ service.title }}</h3>
                <p>{{ service.desc }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 7. Industries We Serve (Bento Grid Sectors) -->
    <section id="industries" class="industries-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">Sectors</span>
          <h2>Tailored for domain standards</h2>
          <p>We configure software environments to meet compliance, data flow, and retention requirements specific to your sector.</p>
        </div>

        <div class="industries-bento">
          <div v-for="(ind, idx) in industries" :key="idx" class="ind-bento-card glass" :class="'ind-' + idx">
            <div class="ind-bento-icon">
              <i :data-lucide="ind.icon"></i>
            </div>
            <h3>{{ ind.name }}</h3>
            <p>{{ ind.desc }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- 8. Why Choose BrightPath (Comparison Grid) -->
    <section class="why-choose-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">Performance Standards</span>
          <h2>How we stack against conventions</h2>
        </div>

        <div class="comparison-grid">
          <div class="comparison-header-labels">
            <span>Engineering Target</span>
            <span>Typical Agencies</span>
            <span class="text-gradient">BrightPath Standard</span>
          </div>

          <div class="comparison-row glass">
            <span class="comp-metric">Initial Design Phase</span>
            <span class="comp-bad">Standard pre-made templates</span>
            <span class="comp-good"><i data-lucide="sparkles"></i> High-fidelity custom design systems</span>
          </div>
          <div class="comparison-row glass">
            <span class="comp-metric">Page Performance</span>
            <span class="comp-bad">Heavy, monolithic architectures (4.2s load)</span>
            <span class="comp-good"><i data-lucide="zap"></i> Optimized Edge Deployment (&lt; 0.6s load)</span>
          </div>
          <div class="comparison-row glass">
            <span class="comp-metric">Backend Infrastructure</span>
            <span class="comp-bad">Basic shared hosting configurations</span>
            <span class="comp-good"><i data-lucide="shield"></i> Auto-scaling, isolated Kubernetes nodes</span>
          </div>
        </div>
      </div>
    </section>

    <!-- 9. Process (Interactive Phase Map) -->
    <section id="process" class="process-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">Workflow</span>
          <h2>The Journey of Construction</h2>
          <p>Our workflow maps clear delivery target lines to eliminate guesswork and delays.</p>
        </div>

        <div class="process-tabs">
          <div 
            v-for="(step, idx) in processSteps" 
            :key="idx" 
            class="process-tab-btn" 
            :class="{ active: activeProcessTab === idx }"
            @click="activeProcessTab = idx"
          >
            <span class="tab-num">0{{ idx + 1 }}</span>
            <span class="tab-name">{{ step.title }}</span>
          </div>
        </div>

        <div class="process-tab-content glass">
          <div class="tab-info">
            <span class="badge badge-accent mb-2">{{ processSteps[activeProcessTab].phase }}</span>
            <h3>{{ processSteps[activeProcessTab].title }}</h3>
            <p>{{ processSteps[activeProcessTab].desc }}</p>
            <ul class="process-subfeatures">
              <li><i data-lucide="arrow-right-circle"></i> Continuous staging reviews</li>
              <li><i data-lucide="arrow-right-circle"></i> Live Slack integrations</li>
            </ul>
          </div>
          <div class="tab-graphic">
            <div class="graphic-blob animate-float">
              <i :data-lucide="processSteps[activeProcessTab].icon" class="graphic-icon"></i>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 10. Featured Projects (Cinematic Cards) -->
    <section id="portfolio" class="portfolio-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">Featured Projects</span>
          <h2>Products built to excel</h2>
        </div>

        <div class="portfolio-cinematic-grid">
          <div 
            v-for="(proj, idx) in projects" 
            :key="idx" 
            class="cinematic-card glass"
          >
            <div class="cinematic-bg-gradient" :style="getGradientStyle(idx)"></div>
            <div class="cinematic-body">
              <span class="badge badge-accent mb-2">{{ proj.category }}</span>
              <h3>{{ proj.title }}</h3>
              <p>{{ proj.desc }}</p>
              
              <div class="cinematic-tech-row">
                <span v-for="tech in proj.stack" :key="tech" class="tech-bubble">{{ tech }}</span>
              </div>

              <div class="cinematic-result-badge">
                <strong>IMPACT:</strong> {{ proj.results }}
              </div>
            </div>
            <div class="cinematic-visual">
              <div class="macbook-frame glass">
                <div class="macbook-screen">
                  <div class="screen-header"><span></span><span></span><span></span></div>
                  <div class="screen-content">
                    <span class="mock-dash-title">{{ proj.title }} API Output</span>
                    <div class="mock-lines">
                      <span class="line-a"></span>
                      <span class="line-b"></span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 11. Technologies -->
    <section class="tech-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">Ecosystem</span>
          <h2>Our Architectural Core</h2>
        </div>

        <div class="tech-scroll-wrapper">
          <div class="tech-scroll">
            <span v-for="tech in techStack" :key="tech" class="tech-logo-card glass">
              {{ tech }}
            </span>
            <!-- Duplicated -->
            <span v-for="tech in techStack" :key="tech + '-dup'" class="tech-logo-card glass">
              {{ tech }}
            </span>
          </div>
        </div>
      </div>
    </section>

    <!-- 12. AI Solutions (Interactive Bento) -->
    <section id="ai-solutions" class="ai-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">Agentic Frameworks</span>
          <h2>Operational AI Solutions</h2>
        </div>

        <div class="ai-bento-grid">
          <div class="ai-bento-card bento-main glass">
            <div class="card-icon"><i data-lucide="bot"></i></div>
            <h3>Custom Autonomous Agents</h3>
            <p>Deploy domain-specific LLM workflows integrated directly into your databases. Automate document sorting, content pipelines, and customer support.</p>
            <div class="interactive-agent-preview glass">
              <div class="agent-preview-header">
                <span class="live-dot"></span>
                <span>bp-agent-core.log</span>
              </div>
              <div class="agent-preview-body">
                <span class="log-entry">> Initializing vector retrieval...</span>
                <span class="log-entry">> Confidence score: 98.4%</span>
                <span class="log-entry">> Payload dispatched successfully.</span>
              </div>
            </div>
          </div>

          <div class="ai-bento-card glass">
            <div class="card-icon"><i data-lucide="line-chart"></i></div>
            <h3>Predictive Systems</h3>
            <p>Forecast business cycles, traffic metrics, and volume demands with high accuracy.</p>
          </div>

          <div class="ai-bento-card glass">
            <div class="card-icon"><i data-lucide="eye"></i></div>
            <h3>Computer Vision</h3>
            <p>Deploy classification algorithms to automate image and asset moderation.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- 13. Testimonials (Large Quote Focus) -->
    <section class="testimonials-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">Verification</span>
          <h2>Endorsements from our partners</h2>
        </div>

        <div class="large-testimonial-slider">
          <div v-for="(t, idx) in testimonials" :key="idx" class="large-test-card glass">
            <i data-lucide="quote" class="quote-icon"></i>
            <p class="test-text">"{{ t.quote }}"</p>
            <div class="test-footer">
              <div class="avatar">{{ t.name.charAt(0) }}</div>
              <div class="details">
                <h4>{{ t.name }}</h4>
                <span>{{ t.role }}, {{ t.company }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 14. Pricing -->
    <section id="pricing" class="pricing-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">Investment Plans</span>
          <h2>Transparent, Value-Focused Rates</h2>
        </div>

        <div class="pricing-flex-grid">
          <div 
            v-for="(plan, idx) in pricingPlans" 
            :key="idx" 
            class="pricing-flex-card glass"
            :class="{ 'featured-plan': plan.featured }"
          >
            <div v-if="plan.featured" class="flex-plan-badge">MOST POPULAR</div>
            <span class="flex-plan-name">{{ plan.name }}</span>
            <div class="flex-plan-price">
              <span class="price-val">{{ plan.price }}</span>
              <span class="price-period" v-if="plan.price !== 'Custom'">/project</span>
            </div>
            <p class="flex-plan-desc">{{ plan.desc }}</p>
            <ul class="flex-plan-features">
              <li v-for="feat in plan.features" :key="feat">
                <i data-lucide="check"></i> {{ feat }}
              </li>
            </ul>
            <a href="#contact" class="btn btn-block" :class="plan.featured ? 'btn-accent' : 'btn-secondary'">Select {{ plan.name }}</a>
          </div>
        </div>
      </div>
    </section>

    <!-- 15. FAQ (Accordion) -->
    <section id="faq" class="faq-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">FAQ</span>
          <h2>Frequently Asked Questions</h2>
        </div>

        <div class="faq-list">
          <div 
            v-for="(faq, idx) in faqs" 
            :key="idx" 
            class="faq-accordion-item glass"
            :class="{ open: activeFaqIndex === idx }"
            @click="activeFaqIndex = activeFaqIndex === idx ? null : idx"
          >
            <div class="faq-item-header">
              <h4>{{ faq.q }}</h4>
              <span class="faq-toggle-icon">
                <i :data-lucide="activeFaqIndex === idx ? 'minus' : 'plus'"></i>
              </span>
            </div>
            <div v-if="activeFaqIndex === idx" class="faq-item-body">
              <p>{{ faq.a }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 16. Journal (Blog) -->
    <section id="blog" class="blog-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">Journal</span>
          <h2>Our Insights & Innovations</h2>
        </div>

        <div class="blog-magazine-grid">
          <div v-for="(post, idx) in blogPosts" :key="idx" class="blog-mag-card glass">
            <span class="blog-mag-tag">{{ post.tag }}</span>
            <h3>{{ post.title }}</h3>
            <p>{{ post.excerpt }}</p>
            <a href="#blog" class="read-more-mag">Read Entry <i data-lucide="arrow-right"></i></a>
          </div>
        </div>
      </div>
    </section>

    <!-- 17. Team -->
    <section class="team-section">
      <div class="container">
        <div class="section-header">
          <span class="badge mb-2">The Studio Collective</span>
          <h2>Engineers, Architects, Designers</h2>
        </div>

        <div class="team-grid">
          <div v-for="(member, idx) in team" :key="idx" class="team-card-profile glass">
            <div class="profile-avatar">{{ member.name.split(' ').map(n => n[0]).join('') }}</div>
            <h4>{{ member.name }}</h4>
            <span>{{ member.role }}</span>
          </div>
        </div>
      </div>
    </section>

    <!-- 18. Contact Form (Cinematic Overlay) -->
    <section id="contact" class="contact-section">
      <div class="container">
        <div class="contact-card-box glass">
          <div class="contact-info">
            <span class="badge badge-accent mb-2">Get in touch</span>
            <h2 class="text-gradient">Ready to build something?</h2>
            <p>Schedule a technology design meeting directly with our leadership team.</p>
            
            <div class="contact-detail-items">
              <div class="detail-item">
                <i data-lucide="mail"></i>
                <span>hello@brightpath.tech</span>
              </div>
              <div class="detail-item">
                <i data-lucide="phone"></i>
                <span>+1 (800) 555-PATH</span>
              </div>
            </div>
          </div>

          <div class="contact-form-area">
            <form @submit.prevent="submitForm">
              <div class="form-row">
                <div class="form-input-group">
                  <label for="name">Name</label>
                  <input type="text" id="name" v-model="form.name" required placeholder="John Doe" />
                </div>
                <div class="form-input-group">
                  <label for="email">Work Email</label>
                  <input type="email" id="email" v-model="form.email" required placeholder="john@company.com" />
                </div>
              </div>
              <div class="form-input-group">
                <label for="project">Requested Solution</label>
                <select id="project" v-model="form.projectType">
                  <option value="Web App">Web Application</option>
                  <option value="Custom Site">Custom Website</option>
                  <option value="AI / LLM">AI Solutions</option>
                  <option value="E-Commerce">E-Commerce</option>
                </select>
              </div>
              <div class="form-input-group">
                <label for="message">Scope Description</label>
                <textarea id="message" v-model="form.message" rows="4" placeholder="Briefly describe what you're building..."></textarea>
              </div>
              <button type="submit" class="btn btn-primary btn-block">
                {{ formSubmitted ? 'Message Dispatched!' : 'Request Proposal' }}
                <i v-if="!formSubmitted" data-lucide="send"></i>
              </button>
            </form>
          </div>
        </div>
      </div>
    </section>

    <!-- 19. Footer -->
    <footer class="footer">
      <div class="container footer-grid">
        <div class="footer-brand">
          <a href="#" class="footer-logo">
            <img src="/logo.svg" alt="BrightPath Logo" class="logo-img" />
            <span>BrightPath</span>
          </a>
          <p>High-end software architectural solutions for startups, scaleups, and enterprises.</p>
          <p class="copyright">&copy; 2026 BrightPath Technologies. All rights reserved.</p>
        </div>
        <div class="footer-column">
          <h4>Capabilities</h4>
          <a href="#services">Custom Web Apps</a>
          <a href="#services">UI/UX Design</a>
          <a href="#ai-solutions">Agentic AI</a>
        </div>
        <div class="footer-column">
          <h4>Sectors</h4>
          <a href="#industries">Healthcare</a>
          <a href="#industries">Real Estate</a>
          <a href="#industries">Finance</a>
        </div>
        <div class="footer-column">
          <h4>Company</h4>
          <a href="#blog">Journal</a>
          <a href="#contact">Contact</a>
        </div>
      </div>
    </footer>

    <!-- Fixed WhatsApp and Meeting CTA -->
    <div class="fixed-cta-container">
      <a href="https://wa.me/1234567890" target="_blank" rel="noopener" class="whatsapp-cta" aria-label="Chat on WhatsApp">
        <svg viewBox="0 0 24 24" width="24" height="24" fill="currentColor">
          <path d="M12.012 2C6.48 2 2 6.48 2 12.012c0 1.764.468 3.48 1.344 5L2 22l5.124-1.344c1.488.816 3.144 1.26 4.884 1.26 5.532 0 10.012-4.48 10.012-10.012C22.02 6.48 17.544 2 12.012 2zm6.24 14.1c-.252.708-1.464 1.296-2.028 1.344-.492.048-.972.24-3.132-.66-2.76-1.152-4.524-3.96-4.656-4.14-.132-.18-.996-1.332-.996-2.544 0-1.212.636-1.8 1.02-2.196.3-.3.792-.372 1.08-.372.288 0 .576 0 .828.012.264.012.612-.108.96.732.36.864 1.224 3.012 1.332 3.228.108.216.18.468.036.756-.144.288-.3.468-.6.816-.3.348-.624.78-.9 1.056-.3.3-.612.624-.264 1.224.348.6 1.548 2.544 3.324 4.128 2.292 2.04 4.224 2.676 4.824 2.976.6.3.96.252 1.32-.156.36-.408 1.548-1.8 1.956-2.424.408-.624.816-.516 1.38-.3.564.216 3.588 1.704 4.188 2.004.6.3.996.444 1.14.684.144.24.144 1.392-.108 2.1z"/>
        </svg>
      </a>
      <a href="#contact" class="book-meeting-cta">
        <i data-lucide="calendar"></i>
        <span>Book Consultation</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      isDarkMode: true,
      isScrolled: false,
      isMobileMenuOpen: false,
      activeServiceIndex: 0,
      activeProcessTab: 0,
      activeFaqIndex: null,
      formSubmitted: false,
      mouseX: 0,
      mouseY: 0,
      heroMouseX: 0,
      heroMouseY: 0,
      form: {
        name: '',
        email: '',
        projectType: 'Web App',
        message: ''
      },
      services: [
        {
          title: 'Custom Website Development',
          icon: 'globe',
          desc: 'High-speed marketing platforms built for absolute conversion and brand prestige.',
          features: ['Next.js App Router Architecture', 'Edge Servers Deployment', 'Perfect PageSpeed Score']
        },
        {
          title: 'SaaS Web Applications',
          icon: 'layout',
          desc: 'Enterprise database products configured with authentication, state management, and unified transaction systems.',
          features: ['Real-time WebSockets', 'OAuth 2.0 Integration', 'Custom RESTful APIs']
        },
        {
          title: 'UI/UX Brand Design',
          icon: 'palette',
          desc: 'High-fidelity Figma architectures, Apple-standard design tokens, and smooth motion graphics.',
          features: ['Design Token Systems', 'Interactive Prototypes', 'Asset Toolkits']
        },
        {
          title: 'AI Solutions & Automation',
          icon: 'cpu',
          desc: 'Operational intelligent flows, vector stores, and custom LLM integrations.',
          features: ['LangChain Integrations', 'Pinecone Vector Databases', 'Agentic Workflows']
        }
      ],
      industries: [
        { name: 'Healthcare', icon: 'heart', desc: 'Secure, HIPAA-compliant patient management panels and health record software.' },
        { name: 'Real Estate', icon: 'home', desc: 'High-prestige property directories featuring virtual maps and interactive asset search.' },
        { name: 'Manufacturing', icon: 'factory', desc: 'Logistics telemetry pipelines, plant automation status monitors, and resource dashboards.' },
        { name: 'Education', icon: 'graduation-cap', desc: 'Modern classrooms, student management setups, and course trackers.' }
      ],
      processSteps: [
        { phase: 'Phase 01', title: 'Discovery & Context', desc: 'Deep research into organizational goals, legacy blockages, and targets.', icon: 'search' },
        { phase: 'Phase 02', title: 'Interactive Design', desc: 'Full clickable prototypes mapping user flow paths and design token properties.', icon: 'palette' },
        { phase: 'Phase 03', title: 'Agile Construction', desc: 'Translating mockups into modern React, Next.js, or Vue repositories.', icon: 'code' },
        { phase: 'Phase 04', title: 'Optimization & Deploy', desc: 'Performance sweeps, pre-flight staging testing, and release configurations.', icon: 'rocket' }
      ],
      projects: [
        {
          title: 'Veloce Logistics Portal',
          category: 'Web Apps',
          desc: 'An enterprise real-time dispatch dashboard built to manage global fleet assets.',
          stack: ['Vue 3', 'Node.js', 'PostgreSQL'],
          results: 'Reduced asset tracking delays by 42%'
        },
        {
          title: 'Ardent AI Assistant',
          category: 'AI/Automation',
          desc: 'A customer support agent processing unstructured legal documents in seconds.',
          stack: ['Next.js', 'OpenAI API', 'Pinecone'],
          results: 'Handled over 50,000 requests without downtime'
        }
      ],
      techStack: ['React', 'Next.js', 'TypeScript', 'Python', 'Django', 'FastAPI', 'Node.js', 'PostgreSQL', 'MongoDB', 'Docker', 'AWS', 'Azure', 'Firebase', 'OpenAI', 'Tailwind CSS'],
      testimonials: [
        {
          quote: "BrightPath delivered our product dashboard two weeks early with outstanding quality. The UI feels like an Apple design.",
          name: "Sarah Jenkins",
          role: "VP of Product",
          company: "Veloce Systems"
        },
        {
          quote: "The backend speed and architectural advice from their architects transformed our API responsiveness completely.",
          name: "Marcus Vance",
          role: "CTO",
          company: "Ardent Tech"
        }
      ],
      pricingPlans: [
        {
          name: 'Starter Sprint',
          price: '$4,999',
          desc: 'Perfect for launching modern landing pages, marketing portals, or early MVP prototypes.',
          features: ['Custom UI Design', 'Next.js Page Scaffold', 'Basic CMS Integration', '2 Sprints of Support'],
          featured: false
        },
        {
          name: 'Scaleup Core',
          price: '$9,999',
          desc: 'Best for custom web platforms, user management, and transactional payment pipelines.',
          features: ['High-Fidelity Wireframes', 'Core Web Application', 'Database Setup', 'Third-Party Integration', '4 Sprints of Support'],
          featured: true
        },
        {
          name: 'Enterprise Plus',
          price: 'Custom',
          desc: 'Engineered for custom AI integrations, legacy migrations, and highly complex architectures.',
          features: ['Dedicated Tech Lead', 'Domain-Tuned LLMs', 'Enterprise SLA Uptime', 'Infinite Support Sprints'],
          featured: false
        }
      ],
      faqs: [
        { q: "What is your typical project timeline?", a: "MVP projects usually ship in 4-6 weeks, while larger enterprise software suites can require 8-12 weeks." },
        { q: "Do we own the software codebase?", a: "Yes, 100% of the Intellectual Property (IP) and custom code belongs to you upon milestone delivery." },
        { q: "Do you offer post-launch maintenance?", a: "Absolutely. We offer flexible SLA-driven maintenance plans covering security audits, performance updates, and new feature Sprints." }
      ],
      blogPosts: [
        { tag: 'Engineering', title: 'Achieving Sub-100ms Page Loads at the Edge', excerpt: 'How we configured Next.js serverless functions to hydrate content globally under 100ms.' },
        { tag: 'Product Design', title: 'The Anatomy of Apple-Level Design Polish', excerpt: 'Breaking down design token setups, micro-animations, and typographic hierarchy.' }
      ],
      team: [
        { name: 'Alex Rivera', role: 'Principal Architect' },
        { name: 'Sofia Chen', role: 'Head of UI/UX' },
        { name: 'David Kojo', role: 'Lead Developer' }
      ]
    };
  },
  computed: {
    spotlightStyle() {
      return {
        left: `${this.mouseX}px`,
        top: `${this.mouseY}px`
      };
    },
    heroVisualRotateStyle() {
      const rx = (this.heroMouseY - 0.5) * -15; // rotate X range [-7.5, 7.5]
      const ry = (this.heroMouseX - 0.5) * 15;  // rotate Y range [-7.5, 7.5]
      return {
        transform: `perspective(1000px) rotateX(${rx}deg) rotateY(${ry}deg)`
      };
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
    window.addEventListener('mousemove', this.handleGlobalMouseMove);
    if (window.lucide) {
      window.lucide.createIcons();
    }
  },
  updated() {
    if (window.lucide) {
      window.lucide.createIcons();
    }
  },
  unmounted() {
    window.removeEventListener('scroll', this.handleScroll);
    window.removeEventListener('mousemove', this.handleGlobalMouseMove);
  },
  methods: {
    handleScroll() {
      this.isScrolled = window.scrollY > 50;
    },
    handleGlobalMouseMove(e) {
      this.mouseX = e.clientX;
      this.mouseY = e.clientY + window.scrollY;
    },
    handleHeroMouseMove(e) {
      const rect = e.currentTarget.getBoundingClientRect();
      this.heroMouseX = (e.clientX - rect.left) / rect.width;
      this.heroMouseY = (e.clientY - rect.top) / rect.height;
    },
    toggleTheme() {
      this.isDarkMode = !this.isDarkMode;
    },
    submitForm() {
      this.formSubmitted = true;
      setTimeout(() => {
        this.form = { name: '', email: '', projectType: 'Web App', message: '' };
        this.formSubmitted = false;
      }, 3000);
    },
    getGradientStyle(index) {
      const gradients = [
        'radial-gradient(circle at top left, rgba(37,99,235,0.2) 0%, transparent 70%)',
        'radial-gradient(circle at top left, rgba(124,58,237,0.2) 0%, transparent 70%)'
      ];
      return {
        background: gradients[index % gradients.length]
      };
    }
  }
};
</script>

<style>
/* Cinematic CSS styling layout modifications for Awwwards-level feel */

.app-wrapper {
  background-color: var(--background);
  color: var(--text);
  transition: var(--transition-smooth);
  width: 100%;
  position: relative;
}

/* Spotlight Cursor */
.cursor-spotlight {
  position: absolute;
  width: 400px;
  height: 400px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(37, 99, 235, 0.05) 0%, transparent 70%);
  pointer-events: none;
  transform: translate(-50%, -50%);
  z-index: 1;
  mix-blend-mode: screen;
}

/* Announcement Bar */
.announcement-bar {
  background: #0B0F19;
  color: #FFFFFF;
  padding: 0.75rem 1rem;
  font-size: 0.85rem;
  text-align: center;
  font-weight: 500;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  flex-wrap: wrap;
  position: relative;
  overflow: hidden;
}

.announcement-glow {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(6, 182, 212, 0.15), transparent);
  animation: slide-infinite 10s linear infinite;
}

.learn-more-link {
  text-decoration: underline;
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  font-weight: 600;
  color: var(--accent);
}

/* Navbar */
.navbar {
  position: sticky;
  top: 0;
  z-index: 100;
  transition: var(--transition-smooth);
}

.navbar.scrolled {
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.05);
  border-bottom: 1px solid var(--border);
}

.nav-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 80px;
}

.nav-logo {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  font-size: 1.25rem;
  font-weight: 800;
  color: var(--dark);
}

.logo-wrapper {
  position: relative;
  width: 36px;
  height: 36px;
}

.logo-img {
  width: 100%;
  height: 100%;
}

.logo-ring {
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  border-radius: 50%;
  border: 1px solid var(--primary);
  opacity: 0.3;
  animation: pulse-slow 3s infinite;
}

.nav-menu {
  display: flex;
  align-items: center;
  gap: 2rem;
}

@media (max-width: 992px) {
  .nav-menu {
    display: none;
  }
}

.nav-link {
  color: var(--muted);
  font-weight: 500;
  font-size: 0.95rem;
  transition: var(--transition-fast);
}

.nav-link:hover {
  color: var(--primary);
}

.nav-actions {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.theme-toggle-btn, .mobile-menu-toggle {
  background: none;
  border: none;
  color: var(--dark);
  cursor: pointer;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: var(--transition-fast);
  border: 1px solid var(--border);
}

.theme-toggle-btn:hover, .mobile-menu-toggle:hover {
  background-color: var(--border);
}

.mobile-menu-toggle {
  display: none;
}

@media (max-width: 992px) {
  .mobile-menu-toggle {
    display: flex;
  }
  .nav-cta {
    display: none;
  }
}

/* Mobile Menu Drawer style */
.mobile-menu {
  position: absolute;
  top: 80px;
  left: 0;
  width: 100%;
  padding: 2rem 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  border-bottom: 1px solid var(--border);
  animation: slideDown 0.3s ease-out forwards;
}

@keyframes slideDown {
  from { transform: translateY(-10px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

/* Hero Section */
.hero-section {
  overflow: hidden;
  padding: 6rem 0;
  position: relative;
  display: flex;
  align-items: center;
  min-height: 80vh;
}

.hero-grid-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: 
    radial-gradient(circle at 1px 1px, var(--border) 1px, transparent 0);
  background-size: 40px 40px;
  opacity: 0.15;
  pointer-events: none;
}

.aurora-blobs {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
  filter: blur(120px);
  z-index: 0;
}

.aurora-blob {
  position: absolute;
  border-radius: 50%;
  opacity: 0.2;
}

.aurora-1 {
  width: 450px;
  height: 450px;
  background-color: var(--primary);
  top: -10%;
  right: 10%;
}

.aurora-2 {
  width: 350px;
  height: 350px;
  background-color: var(--secondary);
  bottom: 10%;
  left: 5%;
}

.aurora-3 {
  width: 300px;
  height: 300px;
  background-color: var(--accent);
  top: 30%;
  left: 40%;
}

.hero-container {
  display: grid;
  grid-template-columns: 1.1fr 1fr;
  gap: 4rem;
  align-items: center;
  position: relative;
  z-index: 1;
}

@media (max-width: 992px) {
  .hero-container {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 3rem;
  }
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}

.hero-title {
  font-size: var(--h1-size);
  font-weight: 800;
  letter-spacing: -0.04em;
  line-height: 1.1;
  margin-bottom: 1.5rem;
}

.hero-subtitle {
  font-size: 1.125rem;
  color: var(--muted);
  margin-bottom: 2rem;
  max-width: 540px;
  line-height: 1.6;
}

@media (max-width: 992px) {
  .hero-subtitle {
    margin-left: auto;
    margin-right: auto;
  }
}

.hero-actions {
  display: flex;
  gap: 1rem;
  margin-bottom: 3rem;
}

@media (max-width: 992px) {
  .hero-actions {
    justify-content: center;
  }
}

@media (max-width: 480px) {
  .hero-actions {
    flex-direction: column;
    width: 100%;
  }
  .hero-actions .btn {
    width: 100%;
  }
}

.hero-metrics {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  border-top: 1px solid var(--border);
  padding-top: 1.5rem;
}

@media (max-width: 992px) {
  .hero-metrics {
    justify-content: center;
  }
}

.hero-divider-dot {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background-color: var(--border);
}

.hero-visual-wrapper {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero-bento-glass {
  width: 100%;
  max-width: 440px;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 30px 60px rgba(0,0,0,0.25);
  transition: transform 0.15s ease-out;
}

.bento-header {
  background-color: rgba(15, 23, 42, 0.4);
  padding: 0.75rem 1.25rem;
  display: flex;
  align-items: center;
  border-bottom: 1px solid var(--border);
}

.bento-dots {
  display: flex;
  gap: 0.4rem;
}

.bento-dots span {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background-color: var(--border);
}

.bento-address {
  margin-left: 1.5rem;
  font-family: monospace;
  font-size: 0.75rem;
  color: var(--muted);
}

.bento-body {
  padding: 1.5rem;
  background-color: rgba(15, 23, 42, 0.2);
}

.code-panel {
  font-family: monospace;
  font-size: 0.8rem;
  color: var(--muted);
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
  margin-bottom: 1.5rem;
}

.keyword { color: var(--secondary); }
.string { color: var(--accent); }

.bento-stats-panel {
  padding: 1rem;
  border-radius: 12px;
}

.bento-stats-header {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.7rem;
  font-weight: 700;
  color: var(--muted);
  margin-bottom: 0.75rem;
}

.indicator-active {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background-color: var(--success);
  box-shadow: 0 0 6px var(--success);
}

.bento-metric-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

.bento-metric-row span {
  display: block;
}

.bento-metric-row .num {
  font-size: 1.25rem;
  font-weight: 800;
}

.bento-metric-row .subtext {
  font-size: 0.7rem;
  color: var(--muted);
}

.floating-tech-badges {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  pointer-events: none;
}

.tech-tag {
  position: absolute;
  font-size: 0.75rem;
  padding: 0.35rem 0.75rem;
  border-radius: 8px;
}

.badge-1 { top: 10%; left: -5%; }
.badge-2 { bottom: 20%; right: -5%; }
.badge-3 { bottom: -5%; left: 10%; }

/* Trusted Partners */
.partner-logo {
  font-size: 1.5rem;
  font-weight: 800;
  color: var(--muted);
  opacity: 0.4;
}

/* Bento Stats Grid */
.stats-bento-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin-top: 2rem;
}

@media (max-width: 992px) {
  .stats-bento-grid {
    grid-template-columns: 1fr;
  }
}

.stats-bento-card {
  padding: 2rem;
  border-radius: 16px;
  border: 1px solid var(--border);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 180px;
  transition: var(--transition-smooth);
}

.stats-bento-card:hover {
  border-color: var(--primary);
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
}

.bento-large {
  grid-column: span 2;
}

@media (max-width: 992px) {
  .bento-large {
    grid-column: span 1;
  }
}

.bento-wide {
  grid-column: span 3;
}

@media (max-width: 992px) {
  .bento-wide {
    grid-column: span 1;
  }
}

.bento-val {
  font-size: 2.5rem;
  font-weight: 800;
  margin-bottom: 0.5rem;
}

.bento-lbl {
  color: var(--muted);
  font-size: 1rem;
}

/* Asymmetric Capabilities Section */
.asymmetric-layout {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  gap: 4rem;
  align-items: flex-start;
}

@media (max-width: 992px) {
  .asymmetric-layout {
    grid-template-columns: 1fr;
  }
}

.asym-left {
  position: sticky;
  top: 120px;
}

.interactive-service-preview {
  padding: 2rem;
  border-radius: 16px;
  min-height: 200px;
}

.preview-title {
  font-size: 0.8rem;
  font-weight: 700;
  color: var(--muted);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  margin-bottom: 1rem;
  display: block;
}

.preview-features {
  list-style: none;
  margin-top: 1rem;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

.preview-features li {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-weight: 600;
}

.preview-features li svg {
  color: var(--success);
  width: 18px;
  height: 18px;
}

.asym-right {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.service-block-card {
  padding: 2rem;
  border-radius: 20px;
  display: flex;
  gap: 1.5rem;
  border: 1px solid var(--border);
  transition: var(--transition-smooth);
  cursor: pointer;
}

.service-block-card:hover {
  border-color: var(--primary);
  transform: translateX(10px);
}

.card-icon-box {
  width: 60px;
  height: 60px;
  border-radius: 16px;
  background-color: rgba(37,99,235,0.1);
  color: var(--primary);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

/* Sectors Bento Grid */
.industries-bento {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.5rem;
}

@media (max-width: 992px) {
  .industries-bento {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 576px) {
  .industries-bento {
    grid-template-columns: 1fr;
  }
}

.ind-bento-card {
  padding: 2.5rem;
  border-radius: 24px;
  border: 1px solid var(--border);
  transition: var(--transition-smooth);
}

.ind-bento-card:hover {
  border-color: var(--accent);
  transform: translateY(-8px);
}

.ind-bento-icon {
  width: 50px;
  height: 50px;
  border-radius: 12px;
  background-color: rgba(6, 182, 212, 0.1);
  color: var(--accent);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
}

.ind-bento-card h3 {
  font-size: 1.25rem;
  margin-bottom: 0.75rem;
}

.ind-bento-card p {
  color: var(--muted);
  font-size: 0.95rem;
}

/* Comparison Grid */
.comparison-grid {
  max-width: 960px;
  margin: 3rem auto 0 auto;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.comparison-header-labels {
  display: grid;
  grid-template-columns: 1.2fr 1fr 1.2fr;
  padding: 0 2rem;
  font-weight: 700;
  color: var(--muted);
  font-size: 0.85rem;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

@media (max-width: 768px) {
  .comparison-header-labels {
    display: none;
  }
}

.comparison-row {
  display: grid;
  grid-template-columns: 1.2fr 1fr 1.2fr;
  padding: 2rem;
  border-radius: 16px;
  border: 1px solid var(--border);
  align-items: center;
}

@media (max-width: 768px) {
  .comparison-row {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
}

.comp-metric {
  font-weight: 700;
}

.comp-bad {
  color: var(--muted);
}

.comp-good {
  color: var(--primary);
  font-weight: 600;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}

/* Process Phase Tabs */
.process-tabs {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-bottom: 3rem;
  flex-wrap: wrap;
}

.process-tab-btn {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.75rem 1.5rem;
  border-radius: 9999px;
  border: 1px solid var(--border);
  cursor: pointer;
  transition: var(--transition-fast);
}

.process-tab-btn.active {
  background-color: var(--primary);
  color: #FFFFFF;
  border-color: var(--primary);
}

.process-tab-btn .tab-num {
  font-weight: 800;
  opacity: 0.6;
}

.process-tab-content {
  display: grid;
  grid-template-columns: 1.2fr 1fr;
  gap: 4rem;
  padding: 4rem;
  border-radius: 24px;
  align-items: center;
}

@media (max-width: 768px) {
  .process-tab-content {
    grid-template-columns: 1fr;
    padding: 2rem;
  }
}

.tab-info h3 {
  font-size: 2rem;
  margin-bottom: 1.5rem;
}

.process-subfeatures {
  list-style: none;
  margin-top: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

.process-subfeatures li {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-weight: 600;
}

.tab-graphic {
  display: flex;
  justify-content: center;
}

.graphic-blob {
  width: 140px;
  height: 140px;
  border-radius: 50%;
  background: linear-gradient(135deg, rgba(37, 99, 235, 0.1), rgba(124, 58, 237, 0.1));
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid var(--border);
}

.graphic-icon {
  width: 64px;
  height: 64px;
  color: var(--primary);
}

/* Cinematic Portfolio Cards */
.portfolio-cinematic-grid {
  display: flex;
  flex-direction: column;
  gap: 4rem;
  margin-top: 3rem;
}

.cinematic-card {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  border-radius: 32px;
  overflow: hidden;
  border: 1px solid var(--border);
  position: relative;
  min-height: 450px;
}

@media (max-width: 992px) {
  .cinematic-card {
    grid-template-columns: 1fr;
  }
}

.cinematic-bg-gradient {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
  pointer-events: none;
}

.cinematic-body {
  padding: 4rem;
  position: relative;
  z-index: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 1.5rem;
}

@media (max-width: 768px) {
  .cinematic-body {
    padding: 2rem;
  }
}

.cinematic-body h3 {
  font-size: 2.25rem;
}

.cinematic-tech-row {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.tech-bubble {
  padding: 0.25rem 0.75rem;
  background-color: var(--surface);
  border: 1px solid var(--border);
  border-radius: 9999px;
  font-size: 0.8rem;
  font-weight: 600;
}

.cinematic-result-badge {
  background-color: rgba(37,99,235,0.1);
  border: 1px solid rgba(37,99,235,0.2);
  color: var(--primary);
  padding: 0.75rem 1rem;
  border-radius: 12px;
  align-self: flex-start;
  font-size: 0.9rem;
}

.cinematic-visual {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 3rem;
  position: relative;
  z-index: 1;
}

.macbook-frame {
  width: 100%;
  max-width: 420px;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 20px 40px rgba(0,0,0,0.25);
  border: 1px solid var(--border);
}

.macbook-screen {
  background-color: #0b0f19;
  height: 220px;
  display: flex;
  flex-direction: column;
}

.screen-header {
  background-color: #04060a;
  padding: 0.5rem;
  display: flex;
  gap: 0.35rem;
}

.screen-header span {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background-color: #333;
}

.screen-content {
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.mock-dash-title {
  color: #fff;
  font-family: monospace;
  font-size: 0.85rem;
}

.mock-lines {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.mock-lines span {
  height: 8px;
  border-radius: 4px;
  background-color: #1e293b;
}

.mock-lines .line-a { width: 90%; }
.mock-lines .line-b { width: 70%; }

/* AI Solution Bento Panel */
.ai-bento-grid {
  display: grid;
  grid-template-columns: 1.5fr 1fr;
  gap: 2rem;
  margin-top: 3rem;
}

@media (max-width: 992px) {
  .ai-bento-grid {
    grid-template-columns: 1fr;
  }
}

.ai-bento-card {
  padding: 3rem;
  border-radius: 28px;
  border: 1px solid var(--border);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.bento-main {
  grid-row: span 2;
}

@media (max-width: 992px) {
  .bento-main {
    grid-row: span 1;
  }
}

.card-icon {
  width: 50px;
  height: 50px;
  border-radius: 12px;
  background-color: rgba(6, 182, 212, 0.1);
  color: var(--accent);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
}

.interactive-agent-preview {
  margin-top: 2rem;
  border-radius: 16px;
  overflow: hidden;
  border: 1px solid var(--border);
}

.agent-preview-header {
  padding: 0.75rem 1rem;
  background-color: rgba(15,23,42,0.4);
  font-family: monospace;
  font-size: 0.75rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.live-dot {
  width: 6px;
  height: 6px;
  background-color: var(--success);
  border-radius: 50%;
  animation: pulse-slow 2s infinite;
}

.agent-preview-body {
  padding: 1.5rem;
  font-family: monospace;
  font-size: 0.8rem;
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
  background-color: rgba(15,23,42,0.2);
}

.log-entry {
  color: var(--muted);
}

/* Large Testimonial Quote Focus */
.large-test-card {
  max-width: 800px;
  margin: 0 auto;
  padding: 4rem;
  border-radius: 32px;
  text-align: center;
  border: 1px solid var(--border);
  position: relative;
}

@media (max-width: 768px) {
  .large-test-card {
    padding: 2rem;
  }
}

.quote-icon {
  width: 48px;
  height: 48px;
  color: var(--primary);
  margin-bottom: 2rem;
  opacity: 0.5;
}

.test-text {
  font-size: 1.5rem;
  font-weight: 500;
  line-height: 1.5;
  margin-bottom: 2.5rem;
  color: var(--dark);
}

@media (max-width: 768px) {
  .test-text {
    font-size: 1.25rem;
  }
}

.test-footer {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
}

.avatar {
  width: 56px;
  height: 56px;
  border-radius: 50%;
  background-color: var(--secondary);
  color: #FFFFFF;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 1.2rem;
}

.details {
  text-align: left;
}

/* Pricing Grid */
.pricing-flex-grid {
  display: flex;
  gap: 2rem;
  margin-top: 3rem;
  justify-content: center;
}

@media (max-width: 992px) {
  .pricing-flex-grid {
    flex-direction: column;
    align-items: center;
  }
}

.pricing-flex-card {
  flex: 1;
  max-width: 380px;
  padding: 3rem 2.5rem;
  border-radius: 28px;
  border: 1px solid var(--border);
  display: flex;
  flex-direction: column;
  position: relative;
}

.pricing-flex-card.featured-plan {
  border-color: var(--primary);
  box-shadow: 0 20px 40px rgba(37,99,235,0.15);
}

.flex-plan-badge {
  position: absolute;
  top: 1.25rem;
  right: 1.25rem;
  background-color: var(--primary);
  color: #FFFFFF;
  padding: 0.25rem 0.75rem;
  border-radius: 9999px;
  font-size: 0.75rem;
  font-weight: 800;
}

.flex-plan-name {
  font-weight: 700;
  color: var(--muted);
  text-transform: uppercase;
  margin-bottom: 1rem;
  display: block;
}

.flex-plan-price {
  display: flex;
  align-items: baseline;
  margin-bottom: 1.5rem;
}

.flex-plan-desc {
  color: var(--muted);
  font-size: 0.95rem;
  margin-bottom: 2rem;
}

.flex-plan-features {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-bottom: 2.5rem;
  border-top: 1px solid var(--border);
  padding-top: 1.5rem;
}

.flex-plan-features li {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  font-size: 0.95rem;
}

.flex-plan-features li svg {
  color: var(--success);
  width: 16px;
  height: 16px;
}

/* Accordion FAQ */
.faq-list {
  max-width: 800px;
  margin: 3rem auto 0 auto;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.faq-accordion-item {
  border-radius: 16px;
  border: 1px solid var(--border);
  cursor: pointer;
}

.faq-item-header {
  padding: 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.faq-toggle-icon {
  color: var(--primary);
}

.faq-item-body {
  padding: 0 2rem 2rem 2rem;
  color: var(--muted);
  font-size: 0.95rem;
}

/* Journal magazine cards */
.blog-magazine-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  margin-top: 3rem;
}

@media (max-width: 768px) {
  .blog-magazine-grid {
    grid-template-columns: 1fr;
  }
}

.blog-mag-card {
  padding: 3rem;
  border-radius: 28px;
  border: 1px solid var(--border);
}

.blog-mag-tag {
  color: var(--secondary);
  font-weight: 700;
  text-transform: uppercase;
  font-size: 0.8rem;
  margin-bottom: 1rem;
  display: block;
}

.blog-mag-card h3 {
  font-size: 1.75rem;
  margin-bottom: 1rem;
  line-height: 1.3;
}

.blog-mag-card p {
  color: var(--muted);
  margin-bottom: 2rem;
}

.read-more-mag {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-weight: 700;
  color: var(--dark);
}

/* Professional Studio Team Profile cards */
.team-card-profile {
  padding: 2rem;
  border-radius: 20px;
  text-align: center;
  border: 1px solid var(--border);
}

.profile-avatar {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  background: linear-gradient(135deg, var(--secondary), var(--accent));
  color: #FFFFFF;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.25rem;
  font-weight: 700;
  margin: 0 auto 1.5rem auto;
}

/* Contact Overlay Bento Box */
.contact-card-box {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  border-radius: 32px;
  overflow: hidden;
  border: 1px solid var(--border);
}

@media (max-width: 992px) {
  .contact-card-box {
    grid-template-columns: 1fr;
  }
}

.contact-info {
  padding: 4rem;
  background-color: rgba(15,23,42,0.2);
  display: flex;
  flex-direction: column;
  justify-content: center;
}

@media (max-width: 768px) {
  .contact-info {
    padding: 2rem;
  }
}

.contact-info h2 {
  font-size: 2.5rem;
  margin-bottom: 1.5rem;
}

.contact-detail-items {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  margin-top: 3rem;
}

.detail-item {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.detail-item svg {
  color: var(--primary);
}

.contact-form-area {
  padding: 4rem;
}

@media (max-width: 768px) {
  .contact-form-area {
    padding: 2rem;
  }
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
}

@media (max-width: 576px) {
  .form-row {
    grid-template-columns: 1fr;
  }
}

.form-input-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  margin-bottom: 1.5rem;
}

.form-input-group label {
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--dark);
}

.form-input-group input, .form-input-group select, .form-input-group textarea {
  padding: 0.75rem 1rem;
  border-radius: 10px;
  border: 1px solid var(--border);
  background-color: var(--background);
  color: var(--text);
  outline: none;
}

.form-input-group input:focus, .form-input-group select:focus, .form-input-group textarea:focus {
  border-color: var(--primary);
}
</style>
