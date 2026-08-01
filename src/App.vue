<template>
  <div class="app-container">
    <header class="page-header container">
      <h1>Enterprise Software Solutions</h1>
      <p>BrightPath Technologies delivers premium engineering services tailored to scale your business operations and drive digital transformation.</p>
    </header>

    <main class="container">
      <section class="services-list">
        
        <!-- Service 1 -->
        <article class="service-block">
          <div class="service-content">
            <span class="service-title">Core Capability</span>
            <h2>Cloud-Native Application Development</h2>
            <p>We architect and build resilient, scalable cloud applications designed to optimize resource consumption and accelerate time-to-market. Our approach ensures seamless integration with modern CI/CD pipelines and high availability architectures.</p>
            
            <h3 class="section-label">Business Benefits</h3>
            <ul class="benefits-list">
              <li>Reduce infrastructure overhead by up to 40%</li>
              <li>Accelerate deployment cycles and feature delivery</li>
              <li>Ensure 99.99% uptime with robust microservices</li>
              <li>Scale dynamically based on user demand</li>
            </ul>

            <a href="#contact" class="cta-button">Discuss Cloud Solutions</a>
          </div>
          
          <div class="service-details">
            <h3 class="section-label">Engineering Process</h3>
            <p>Discovery & Architecture → Microservices Design → Implementation & Testing → Automated Deployment.</p>
            
            <h3 class="section-label">Technologies</h3>
            <div class="tech-tags">
              <span class="tech-tag">AWS</span>
              <span class="tech-tag">Kubernetes</span>
              <span class="tech-tag">Docker</span>
              <span class="tech-tag">Go</span>
              <span class="tech-tag">Node.js</span>
            </div>
            
            <div class="case-study">
              <h4>Case Study: FinTech Scaling</h4>
              <p>Migrated a legacy monolithic banking application to a distributed microservices architecture, handling a 300% increase in daily transaction volume without degradation.</p>
            </div>
          </div>
        </article>

        <!-- Service 2 -->
        <article class="service-block">
          <div class="service-content">
            <span class="service-title">Strategic Offering</span>
            <h2>Enterprise Data Integration & Analytics</h2>
            <p>Transform fragmented data silos into a unified intelligence ecosystem. We engineer secure data pipelines and analytical platforms that empower real-time decision-making and operational transparency.</p>
            
            <h3 class="section-label">Business Benefits</h3>
            <ul class="benefits-list">
              <li>Centralize cross-departmental data governance</li>
              <li>Enable predictive analytics for supply chain forecasting</li>
              <li>Reduce reporting time from days to minutes</li>
              <li>Maintain strict compliance with data regulations</li>
            </ul>

            <a href="#contact" class="cta-button">Explore Data Integration</a>
          </div>
          
          <div class="service-details">
            <h3 class="section-label">Engineering Process</h3>
            <p>Data Audit → Pipeline Architecture → ETL/ELT Implementation → Visualization & Handover.</p>
            
            <h3 class="section-label">Technologies</h3>
            <div class="tech-tags">
              <span class="tech-tag">Snowflake</span>
              <span class="tech-tag">Apache Kafka</span>
              <span class="tech-tag">Python</span>
              <span class="tech-tag">dbt</span>
              <span class="tech-tag">PowerBI</span>
            </div>
            
            <div class="case-study">
              <h4>Case Study: Retail Analytics</h4>
              <p>Deployed a real-time inventory tracking and prediction engine for a national retailer, reducing stockouts by 22% within the first quarter.</p>
            </div>
          </div>
        </article>

        <!-- Service 3 -->
        <article class="service-block">
          <div class="service-content">
            <span class="service-title">Modernization</span>
            <h2>Legacy System Modernization</h2>
            <p>Strategically transition aging infrastructure to modern paradigms without disrupting ongoing operations. We mitigate technical debt while introducing robust security and maintainability frameworks.</p>
            
            <h3 class="section-label">Business Benefits</h3>
            <ul class="benefits-list">
              <li>Eliminate licensing costs for outdated proprietary software</li>
              <li>Enhance enterprise security posture against modern threats</li>
              <li>Improve developer productivity and code maintainability</li>
              <li>Enable integration with external APIs and partner ecosystems</li>
            </ul>

            <a href="#contact" class="cta-button">Start Modernization</a>
          </div>
          
          <div class="service-details">
            <h3 class="section-label">Engineering Process</h3>
            <p>System Assessment → Strangler Fig Strategy → Incremental Refactoring → Final Cutover.</p>
            
            <h3 class="section-label">Technologies</h3>
            <div class="tech-tags">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">React</span>
              <span class="tech-tag">Java Spring Boot</span>
              <span class="tech-tag">PostgreSQL</span>
              <span class="tech-tag">Terraform</span>
            </div>
            
            <div class="case-study">
              <h4>Case Study: Healthcare ERP Migration</h4>
              <p>Successfully modernized a 15-year-old on-premise ERP to a cloud-hosted platform, achieving zero downtime and full HIPAA compliance.</p>
            </div>
          </div>
        </article>

      </section>
    </main>
    
    <footer class="footer">
      <div class="container">
        <p>&copy; 2026 BrightPath Technologies. Premium Engineering Services.</p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style>
/* Any local specific styles if needed, though most are in index.css */
</style>
