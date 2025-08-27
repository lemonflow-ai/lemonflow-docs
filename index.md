---
title: 🍋 Lemonflow.docs
layout: default
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Raleway:wght@400;450;500;600;700&display=swap');
  
  h1 {
    font-family: 'Raleway', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif !important;
    font-weight: 700 !important;
    font-size: 3rem !important;
    margin-bottom: 1.5rem !important;
    background: linear-gradient(135deg, #1FB270 0%, #8fd3f4 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    font-variant-ligatures: normal !important;
    -webkit-font-variant-ligatures: normal !important;
  }
  
  .site-title {
    font-family: 'Raleway', sans-serif !important;
  }
  
  .site-title .lemon {
    font-weight: 600 !important;
  }
  
  .site-title .docs {
    font-weight: 450 !important;
  }
  
  .docs, body {
    font-family: 'Raleway', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif !important;
    font-weight: 450 !important;
    line-height: 1.7 !important;
    font-variant-ligatures: normal !important;
    -webkit-font-variant-ligatures: normal !important;
    font-feature-settings: "liga" 1 !important;
  }
  
  .service-card {
    margin: 2.5rem 0;
    padding: 2.5rem;
    background: linear-gradient(135deg, #ffffff 0%, #f8f9fa 100%);
    border-radius: 20px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    border: 1px solid rgba(31, 178, 112, 0.1);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    position: relative;
    overflow: hidden;
  }
  
  .service-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, #1FB270 0%, #8fd3f4 100%);
    transform: scaleX(0);
    transition: transform 0.3s;
  }
  
  .service-card:hover {
    box-shadow: 0 8px 25px rgba(31, 178, 112, 0.15);
    border-color: rgba(31, 178, 112, 0.3);
  }
  
  .service-card:hover::before {
    transform: scaleX(1);
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
    background: linear-gradient(135deg, #e7f5e7 0%, #d4f4dd 100%);
    color: #1FB270;
    font-weight: 600;
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
    padding: 1rem 2rem;
    background: linear-gradient(135deg, #1FB270 0%, #17a060 100%);
    color: #ffffff !important;
    text-decoration: none;
    border-radius: 40px;
    font-weight: 600;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    margin-top: 1.5rem;
    box-shadow: 0 4px 12px rgba(31, 178, 112, 0.3);
  }
  
  .cta-button:hover {
    background: linear-gradient(135deg, #17a060 0%, #1FB270 100%);
    box-shadow: 0 6px 20px rgba(31, 178, 112, 0.4);
    font-weight: 700;
    text-decoration: underline;
    color: #ffffff !important;
  }
  
  .button-wrapper {
    text-align: center;
    margin-top: 1.5rem;
  }
  
  footer {
    background: linear-gradient(135deg, #f8f9fa 0%, #ffffff 100%);
    color: #333;
    padding: 4rem 2rem 2rem 2rem;
    margin-top: 6rem;
    text-align: center;
    position: relative;
    border-top: 1px solid #e0e0e0;
  }
  
  footer::before {
    content: '';
    position: absolute;
    top: -1px;
    left: 10%;
    right: 10%;
    height: 3px;
    background: linear-gradient(90deg, #1FB270 0%, #8fd3f4 100%);
    border-radius: 2px;
  }
  
  .footer-link {
    color: #0066cc !important;
    text-decoration: none !important;
    transition: all 0.3s;
    border-bottom: 1px solid transparent;
  }
  
  .footer-link:hover {
    color: #1FB270 !important;
    border-bottom-color: #1FB270;
  }
  
  .service-name {
    font-family: 'Raleway', sans-serif;
  }
  
  .service-name .name {
    font-weight: 600;
    color: #1a1a1a;
  }
  
  .service-name .type {
    font-weight: 400;
    color: #666;
    font-size: 0.9em;
  }
</style>

<div class="docs">

<p style="font-size: 1.2rem; color: #4a4a4a; margin: 2rem 0; line-height: 1.8;">
Welcome to the public documentation for Lemonflow.ai services. Here you'll find integration guides, API references, and troubleshooting information for all of our AI-powered customer service solutions.
</p>

<h2 style="font-size: 2rem; margin: 3rem 0 2rem 0; color: #2c2c2c;">Technical Documentation</h2>

<div class="service-card">
  <h3 style="font-size: 1.5rem; margin-bottom: 1rem; color: #1a1a1a;">
    <span class="service-name">
      💬 <span class="name">.chat</span> <span class="type">(widget)</span>
    </span>
    <span class="status-badge status-available">✅ Documentation up to date</span>
  </h3>
  
  <p style="color: #5a5a5a; margin-bottom: 1.5rem; line-height: 1.6;">
    Embed our intelligent AI engine directly into your website or mobile application. Seamlessly integrates with your brand, providing instant 24/7 customer support with remote actions. 
  </p>
  
  <h4 style="font-size: 1rem; margin-bottom: 0.75rem; color: #3a3a3a;">Key Features:</h4>
  <ul class="feature-list" style="color: #666; line-height: 1.8;">
    <li>Simple integration, only 2 lines of HTML code required</li>
    <li>Mobile-first responsive design</li>
    <li>Automatically inherits your brand colors & styling</li>
    <li>Accessiblity compliant (WCAG 2.1 AA)</li>
    <li>Full capabilities of the Lemonflow engine</li>
  </ul>
  
  <div class="button-wrapper">
    <a href="widget/integration" class="cta-button">View Integration Guide</a>
  </div>
</div>

<div class="service-card">
  <h3 style="font-size: 1.5rem; margin-bottom: 1rem; color: #1a1a1a;">
    <span class="service-name">
      📱 <span class="name">.chat</span> <span class="type">(whatsapp)</span>
    </span>
    <span class="status-badge status-coming">🔄 Documentation coming soon</span>
  </h3>
  
  <p style="color: #5a5a5a; margin-bottom: 1.5rem; line-height: 1.6;">
    Meet your customers where they are. Deploy our intelligent AI engine directly from within WhatsApp.
  </p>
  
  <h4 style="font-size: 1rem; margin-bottom: 0.75rem; color: #3a3a3a;">Key Features:</h4>
  <ul class="feature-list" style="color: #666; line-height: 1.8;">
    <li>Official WhatsApp Business API integration</li>
    <li>Rich media support (images, documents, voice notes)</li>
    <li>Interactive buttons & quick replies</li>
  </ul>
  
  <p style="color: #888; font-style: italic; margin-top: 1.5rem;">
    Documentation in development - Expected Q4 2025
  </p>
</div>

<div class="service-card">
  <h3 style="font-size: 1.5rem; margin-bottom: 1rem; color: #1a1a1a;">
    <span class="service-name">
      📧 <span class="name">.email</span>
    </span>
    <span class="status-badge status-coming">🔄 Documentation coming soon</span>
  </h3>
  
  <p style="color: #5a5a5a; margin-bottom: 1.5rem; line-height: 1.6;">
    Transform your email support with AI that understands context and urgency. Our email assistant drafts personalized responses, categorizes inquiries, and seamlessly escalates complex issues.
  </p>
  
  <h4 style="font-size: 1rem; margin-bottom: 0.75rem; color: #3a3a3a;">Key Features:</h4>
  <ul class="feature-list" style="color: #666; line-height: 1.8;">
    <li>Contextual response generation with brand voice</li>
    <li>Seamless CRM & helpdesk integration</li>
    <li>Human-in-the-loop approval workflows</li>
    <li>Multi-language support with translation</li>
    <li>Smart attachement handling</li>
  </ul>
  
  <p style="color: #888; font-style: italic; margin-top: 1.5rem;">
    Documentation in development - Expected Q4 2025
  </p>
</div>

</div>
