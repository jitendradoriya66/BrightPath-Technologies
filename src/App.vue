<template>
  <div class="ds-dashboard">
    <header class="ds-header">
      <div class="container flex justify-between items-center">
        <div class="ds-logo">BrightPath <span>Design System</span></div>
        <div class="ds-version">v2.0.0</div>
      </div>
    </header>

    <div class="container ds-layout">
      <!-- Sidebar Navigation -->
      <aside class="ds-sidebar">
        <nav>
          <a href="#logo">Logo Refinement</a>
          <a href="#colors">Color Palette</a>
          <a href="#typography">Typography Scale</a>
          <a href="#spacing">Spacing System</a>
          <a href="#grid">Grid System</a>
          <a href="#components">Components</a>
          <a href="#animations">Animations</a>
        </nav>
      </aside>

      <!-- Main Content -->
      <main class="ds-content">
        <!-- Logo -->
        <section id="logo" class="ds-section">
          <h2>Logo Refinement</h2>
          <p>The primary mark of BrightPath Technologies.</p>
          <div class="card flex items-center gap-4">
            <svg width="48" height="48" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg">
              <rect width="48" height="48" rx="8" fill="#2563eb"/>
              <path d="M14 24L22 32L34 16" stroke="white" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            <div>
              <h3 class="mb-1">BrightPath</h3>
              <p class="caption m-0">Corporate Logomark &amp; Typography</p>
            </div>
          </div>
        </section>

        <!-- Colors -->
        <section id="colors" class="ds-section">
          <h2>Color Palette</h2>
          <p>Semantic colors ensuring high contrast and professional aesthetic.</p>
          <div class="grid-3">
            <div class="color-card">
              <div class="color-swatch" style="background: var(--color-slate)"></div>
              <div class="p-2">
                <strong>Slate</strong>
                <p class="caption">#0f172a / --color-slate</p>
              </div>
            </div>
            <div class="color-card">
              <div class="color-swatch" style="background: var(--color-charcoal)"></div>
              <div class="p-2">
                <strong>Charcoal</strong>
                <p class="caption">#1e293b / --color-charcoal</p>
              </div>
            </div>
            <div class="color-card">
              <div class="color-swatch" style="background: var(--color-blue)"></div>
              <div class="p-2">
                <strong>Blue</strong>
                <p class="caption">#2563eb / --color-blue</p>
              </div>
            </div>
            <div class="color-card">
              <div class="color-swatch border" style="background: var(--color-bg)"></div>
              <div class="p-2">
                <strong>Background</strong>
                <p class="caption">#020617 / --color-bg</p>
              </div>
            </div>
            <div class="color-card">
              <div class="color-swatch border" style="background: var(--color-border)"></div>
              <div class="p-2">
                <strong>Border</strong>
                <p class="caption">#334155 / --color-border</p>
              </div>
            </div>
          </div>
        </section>

        <!-- Typography -->
        <section id="typography" class="ds-section">
          <h2>Typography Scale</h2>
          <p>Strict scaling based on an 8pt modular system.</p>
          <div class="card flex flex-col gap-4">
            <div>
              <h1>Heading 1</h1>
              <p class="caption">3rem (48px) / Bold</p>
            </div>
            <div>
              <h2>Heading 2</h2>
              <p class="caption">2.25rem (36px) / Bold</p>
            </div>
            <div>
              <h3>Heading 3</h3>
              <p class="caption">1.5rem (24px) / Bold</p>
            </div>
            <div>
              <h4>Heading 4</h4>
              <p class="caption">1.25rem (20px) / Bold</p>
            </div>
            <div>
              <p>Body text. We build high-performance, scalable web applications that drive enterprise conversion and growth. Partner with a premium software engineering team.</p>
              <p class="caption">1rem (16px) / Regular</p>
            </div>
            <div>
              <span class="caption">Caption text. Used for meta-information.</span>
              <p class="caption mt-1">0.875rem (14px) / Regular</p>
            </div>
          </div>
        </section>

        <!-- Spacing -->
        <section id="spacing" class="ds-section">
          <h2>Spacing System</h2>
          <p>Base-8 spatial units for consistent padding and margins.</p>
          <div class="card">
            <div class="spacing-demo flex items-center mb-2">
              <div class="spacing-block" style="width: var(--spacing-1)"></div>
              <span class="caption ml-2">--spacing-1 (8px)</span>
            </div>
            <div class="spacing-demo flex items-center mb-2">
              <div class="spacing-block" style="width: var(--spacing-2)"></div>
              <span class="caption ml-2">--spacing-2 (16px)</span>
            </div>
            <div class="spacing-demo flex items-center mb-2">
              <div class="spacing-block" style="width: var(--spacing-3)"></div>
              <span class="caption ml-2">--spacing-3 (24px)</span>
            </div>
            <div class="spacing-demo flex items-center mb-2">
              <div class="spacing-block" style="width: var(--spacing-4)"></div>
              <span class="caption ml-2">--spacing-4 (32px)</span>
            </div>
            <div class="spacing-demo flex items-center mb-2">
              <div class="spacing-block" style="width: var(--spacing-5)"></div>
              <span class="caption ml-2">--spacing-5 (40px)</span>
            </div>
            <div class="spacing-demo flex items-center mb-2">
              <div class="spacing-block" style="width: var(--spacing-6)"></div>
              <span class="caption ml-2">--spacing-6 (48px)</span>
            </div>
            <div class="spacing-demo flex items-center mb-2">
              <div class="spacing-block" style="width: var(--spacing-8)"></div>
              <span class="caption ml-2">--spacing-8 (64px)</span>
            </div>
            <div class="spacing-demo flex items-center">
              <div class="spacing-block" style="width: var(--spacing-12)"></div>
              <span class="caption ml-2">--spacing-12 (96px)</span>
            </div>
          </div>
        </section>

        <!-- Grid System -->
        <section id="grid" class="ds-section">
          <h2>Grid System Preview</h2>
          <p>12-column liquid layout standard.</p>
          <div class="grid-12 mb-4">
            <div class="grid-col" v-for="n in 12" :key="n">1</div>
          </div>
          <div class="grid-12 mb-4">
            <div class="grid-col" style="grid-column: span 4;">4</div>
            <div class="grid-col" style="grid-column: span 4;">4</div>
            <div class="grid-col" style="grid-column: span 4;">4</div>
          </div>
          <div class="grid-12">
            <div class="grid-col" style="grid-column: span 3;">3</div>
            <div class="grid-col" style="grid-column: span 6;">6</div>
            <div class="grid-col" style="grid-column: span 3;">3</div>
          </div>
        </section>

        <!-- Components -->
        <section id="components" class="ds-section">
          <h2>Reusable Components</h2>
          <p>UI elements designed for conversion and clarity.</p>

          <h3 class="mb-2">Buttons</h3>
          <div class="card flex gap-4 items-center mb-4">
            <button class="btn">Primary Action</button>
            <button class="btn btn-secondary">Secondary Action</button>
          </div>

          <h3 class="mb-2">Badges</h3>
          <div class="card flex gap-2 mb-4">
            <span class="badge">New</span>
            <span class="badge">Enterprise</span>
            <span class="badge">Stable</span>
          </div>

          <h3 class="mb-2">Inputs &amp; Forms</h3>
          <div class="card mb-4" style="max-width: 400px;">
            <div class="form-group">
              <label class="form-label">Email Address</label>
              <input type="email" class="form-control" placeholder="user@corporate.com" />
            </div>
            <div class="form-group mb-0">
              <label class="form-label">Password</label>
              <input type="password" class="form-control" value="password" />
            </div>
          </div>

          <h3 class="mb-2">Navigation Bar</h3>
          <div class="card mb-4 nav-preview flex items-center justify-between p-4">
            <div class="font-bold">Brand</div>
            <div class="flex gap-4">
              <a href="#" class="caption">Features</a>
              <a href="#" class="caption">Pricing</a>
              <a href="#" class="caption">Docs</a>
            </div>
          </div>

          <h3 class="mb-2">Tabs</h3>
          <div class="card mb-4 p-0 overflow-hidden">
            <div class="flex border-b">
              <div class="tab active">Overview</div>
              <div class="tab">Settings</div>
              <div class="tab">Billing</div>
            </div>
            <div class="p-4">
              <p class="m-0">Tab content panel.</p>
            </div>
          </div>

          <h3 class="mb-2">Accordion</h3>
          <div class="card p-0">
            <div class="accordion-item p-4 border-b">
              <div class="flex justify-between items-center">
                <strong>What is the SLA?</strong>
                <span>+</span>
              </div>
            </div>
            <div class="accordion-item p-4">
              <div class="flex justify-between items-center">
                <strong>How does billing work?</strong>
                <span>+</span>
              </div>
            </div>
          </div>
        </section>

        <!-- Animations -->
        <section id="animations" class="ds-section">
          <h2>Easing Animations</h2>
          <p>Micro-interactions to reinforce feedback loops without distraction.</p>
          <div class="card flex gap-4">
            <div class="anim-box hover-scale">Scale on Hover</div>
            <div class="anim-box hover-lift">Lift on Hover</div>
          </div>
        </section>

      </main>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DesignSystem'
}
</script>

<style scoped>
.ds-dashboard {
  min-height: 100vh;
}
.ds-header {
  padding: var(--spacing-3) 0;
  border-bottom: 1px solid var(--color-border);
  background-color: var(--color-bg);
  position: sticky;
  top: 0;
  z-index: 100;
}
.ds-logo {
  font-weight: 700;
  font-size: var(--font-h4);
}
.ds-logo span {
  font-weight: 400;
  color: var(--color-text-muted);
}
.ds-version {
  font-family: monospace;
  font-size: var(--font-caption);
  color: var(--color-text-muted);
  background: var(--color-charcoal);
  padding: 4px 8px;
  border-radius: var(--border-radius);
}
.ds-layout {
  display: flex;
  align-items: flex-start;
  gap: var(--spacing-8);
  padding-top: var(--spacing-8);
  padding-bottom: var(--spacing-8);
}
.ds-sidebar {
  width: 240px;
  flex-shrink: 0;
  position: sticky;
  top: 100px;
}
.ds-sidebar nav {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-2);
}
.ds-sidebar nav a {
  color: var(--color-text-muted);
  font-weight: 500;
  padding: var(--spacing-1) var(--spacing-2);
  border-radius: var(--border-radius);
  margin-left: calc(var(--spacing-2) * -1);
}
.ds-sidebar nav a:hover {
  background: var(--color-charcoal);
  color: var(--color-text);
}
.ds-content {
  flex-grow: 1;
  min-width: 0;
}
.ds-section {
  margin-bottom: var(--spacing-12);
}
.color-card {
  background: var(--color-slate);
  border: 1px solid var(--color-border);
  border-radius: var(--border-radius);
  overflow: hidden;
}
.color-swatch {
  height: 100px;
  width: 100%;
}
.color-swatch.border {
  border-bottom: 1px solid var(--color-border);
}
.m-0 { margin: 0 !important; }
.ml-2 { margin-left: var(--spacing-2); }
.mt-1 { margin-top: var(--spacing-1); }
.spacing-block {
  height: 32px;
  background-color: var(--color-blue);
  border-radius: 2px;
}
.grid-col {
  background: var(--color-charcoal);
  border: 1px solid var(--color-border);
  padding: var(--spacing-2);
  text-align: center;
  border-radius: 2px;
  font-size: var(--font-caption);
  color: var(--color-text-muted);
}
.border-b {
  border-bottom: 1px solid var(--color-border);
}
.overflow-hidden {
  overflow: hidden;
}
.font-bold {
  font-weight: 700;
}
.nav-preview {
  background: var(--color-charcoal);
}
.tab {
  padding: var(--spacing-2) var(--spacing-4);
  font-size: var(--font-caption);
  color: var(--color-text-muted);
  cursor: pointer;
  border-bottom: 2px solid transparent;
}
.tab.active {
  color: var(--color-text);
  border-bottom-color: var(--color-blue);
}
.accordion-item:last-child {
  border-bottom: none;
}
.anim-box {
  width: 120px;
  height: 120px;
  background: var(--color-charcoal);
  border: 1px solid var(--color-border);
  border-radius: var(--border-radius);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  font-size: var(--font-caption);
  cursor: pointer;
  transition: var(--transition);
}
.hover-scale:hover {
  transform: scale(1.05);
  border-color: var(--color-blue);
}
.hover-lift:hover {
  transform: translateY(-8px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.5);
  border-color: var(--color-blue);
}

@media (max-width: 900px) {
  .ds-layout {
    flex-direction: column;
  }
  .ds-sidebar {
    width: 100%;
    position: static;
  }
}
</style>
