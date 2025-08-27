---
title: 🍋 Lemonflow.docs
---

<style>
  h1 {
    font-family: 'Raleway', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif !important;
    font-weight: 600 !important;
    font-size: 2.5rem !important;
    margin-bottom: 1.5rem !important;
    color: #1a1a1a !important;
  }
  
  .docs, body {
    font-family: 'Raleway', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif !important;
    font-weight: 450 !important;
    line-height: 1.7 !important;
  }
  
  .service-card {
    margin: 2.5rem 0;
    padding: 2rem;
    background: #ffffff;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    border: 1px solid #e8e8e8;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  
  .service-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
  }
  
  .status-badge {
    display: inline-block;
    padding: 0.25rem 0.75rem;
    border-radius: 20px;
    font-size: 0.875rem;
    font-weight: 500;
    margin-left: 0.5rem;
  }
  
  .status-available {
    background: #e7f5e7;
    color: #2e7d2e;
  }
  
  .status-coming {
    background: #fff4e5;
    color: #c96100;
  }
  
  .feature-list {
    margin: 1rem 0;
    padding-left: 1.5rem;
  }
  
  .cta-button {
    display: inline-block;
    padding: 0.75rem 1.5rem;
    background: #ffd700;
    color: #1a1a1a;
    text-decoration: none;
    border-radius: 8px;
    font-weight: 500;
    transition: background 0.2s;
    margin-top: 1rem;
  }
  
  .cta-button:hover {
    background: #ffed4e;
  }
  
  .contact-section {
    background: #f8f9fa;
    padding: 2rem;
    border-radius: 12px;
    margin: 3rem 0 2rem 0;
    text-align: center;
  }
</style>

<div class="docs">

<p style="font-size: 1.2rem; color: #4a4a4a; margin: 2rem 0; line-height: 1.8;">
Welcome to the public documentation for <strong>Lemonflow.ai</strong> services. Here you'll find integration guides, API references, and troubleshooting information for all of our AI-powered customer service solutions.
</p>

<h2 style="font-size: 2rem; margin: 3rem 0 2rem 0; color: #2c2c2c;">Available Services</h2>

<div class="service-card">
  <h3 style="font-size: 1.5rem; margin-bottom: 1rem; color: #1a1a1a;">
    💬 Chat Widget 
    <span class="status-badge status-available">✅ Available</span>
  </h3>
  
  <p style="color: #5a5a5a; margin-bottom: 1.5rem;">
    Professional chat widget for websites with smart branding and accessibility features.
  </p>
  
  <h4 style="font-size: 1rem; margin-bottom: 0.75rem; color: #3a3a3a;">Key Features:</h4>
  <ul class="feature-list">
    <li>WCAG 2.1 AA compliant accessibility</li>
    <li>Smart brand color inheritance</li>
    <li>Mobile responsive design</li>
    <li>Keyboard navigation support</li>
    <li>Real-time customer support</li>
  </ul>
  
  <a href="widget/integration" class="cta-button">📖 View Integration Guide</a>
</div>

<div class="service-card">
  <h3 style="font-size: 1.5rem; margin-bottom: 1rem; color: #1a1a1a;">
    📧 Email Responder
    <span class="status-badge status-coming">🔄 Coming Soon</span>
  </h3>
  
  <p style="color: #5a5a5a; margin-bottom: 1.5rem;">
    Automated email response system powered by Gemini 2.5 Pro for intelligent customer service.
  </p>
  
  <h4 style="font-size: 1rem; margin-bottom: 0.75rem; color: #3a3a3a;">Key Features:</h4>
  <ul class="feature-list">
    <li>Multi-language support</li>
    <li>Intelligent email routing and categorization</li>
    <li>Assessment integration</li>
    <li>Automated response generation</li>
    <li>Custom workflow management</li>
  </ul>
  
  <p style="color: #888; font-style: italic; margin-top: 1.5rem;">
    Documentation in development - Expected Q1 2025
  </p>
</div>

<div class="service-card">
  <h3 style="font-size: 1.5rem; margin-bottom: 1rem; color: #1a1a1a;">
    📱 WhatsApp Integration
    <span class="status-badge status-coming">🔄 Coming Soon</span>
  </h3>
  
  <p style="color: #5a5a5a; margin-bottom: 1.5rem;">
    WhatsApp Business API integration for seamless customer support via messaging.
  </p>
  
  <h4 style="font-size: 1rem; margin-bottom: 0.75rem; color: #3a3a3a;">Key Features:</h4>
  <ul class="feature-list">
    <li>Rich messaging with media support</li>
    <li>Automated response workflows</li>
    <li>Business API integration</li>
    <li>Multi-agent support</li>
    <li>Message history and analytics</li>
  </ul>
  
  <p style="color: #888; font-style: italic; margin-top: 1.5rem;">
    Documentation in development - Expected Q2 2025
  </p>
</div>

<div class="contact-section">
  <h2 style="font-size: 1.75rem; margin-bottom: 1.5rem; color: #2c2c2c;">Need Help?</h2>
  
  <p style="color: #5a5a5a; margin-bottom: 2rem;">
    Our technical team is here to assist with integration questions and troubleshooting.
  </p>
  
  <div style="display: flex; justify-content: center; gap: 3rem; flex-wrap: wrap;">
    <div>
      <strong style="color: #3a3a3a;">📧 Technical Support</strong><br>
      <a href="mailto:tech@lemonflow.ai" style="color: #0066cc; text-decoration: none;">tech@lemonflow.ai</a>
    </div>
    <div>
      <strong style="color: #3a3a3a;">🌐 Website</strong><br>
      <a href="https://lemonflow.ai/" style="color: #0066cc; text-decoration: none;">lemonflow.ai</a>
    </div>
    <div>
      <strong style="color: #3a3a3a;">📚 Documentation</strong><br>
      <span style="color: #666;">You're already here!</span>
    </div>
  </div>
</div>

<div style="text-align: center; color: #888; font-size: 0.875rem; margin-top: 3rem; padding-top: 1.5rem; border-top: 1px solid #e0e0e0;">
  <p style="margin: 0;"><em>Last updated: August 2025</em></p>
</div>

</div>