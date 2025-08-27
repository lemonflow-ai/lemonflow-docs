---
title: .chat Widget Integration Guide
layout: default
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Raleway:wght@400;450;500;600;700&display=swap');
  
  body {
    font-family: 'Raleway', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    font-weight: 450;
    line-height: 1.7;
    font-variant-ligatures: normal;
    -webkit-font-variant-ligatures: normal;
    font-feature-settings: "liga" 1;
    color: #333;
  }
  
  h1 {
    font-family: 'Raleway', sans-serif;
    font-weight: 700;
    font-size: 2.5rem;
    margin: 3rem 0 1.5rem 0;
    background: linear-gradient(135deg, #1FB270 0%, #8fd3f4 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  
  h2 {
    font-family: 'Raleway', sans-serif;
    font-weight: 600;
    font-size: 1.8rem;
    color: #2c2c2c;
    margin: 3rem 0 1.5rem 0;
    padding-top: 2rem;
    border-top: 2px solid #f0f0f0;
  }
  
  h3 {
    font-family: 'Raleway', sans-serif;
    font-weight: 600;
    font-size: 1.4rem;
    color: #3a3a3a;
    margin: 2rem 0 1rem 0;
  }
  
  h4 {
    font-family: 'Raleway', sans-serif;
    font-weight: 600;
    font-size: 1.2rem;
    color: #3a3a3a;
    margin: 1.5rem 0 1rem 0;
  }
  
  .back-nav {
    background: linear-gradient(135deg, #f8f9fa 0%, #ffffff 100%);
    padding: 1rem 1.5rem;
    margin-bottom: 3rem;
    border-radius: 12px;
    font-size: 0.95rem;
    border: 1px solid #e0e0e0;
    display: inline-block;
  }
  
  .back-nav a {
    color: #1FB270;
    text-decoration: none;
    font-weight: 500;
    transition: all 0.3s;
  }
  
  .back-nav a:hover {
    color: #17a060;
    text-decoration: underline;
  }
  
  .intro-text {
    font-size: 1.2rem;
    color: #4a4a4a;
    margin: 2rem 0 3rem 0;
    line-height: 1.8;
  }
  
  pre {
    background: #f8f9fa;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    padding: 1.5rem;
    margin: 2rem 0;
    overflow-x: auto;
    font-size: 0.95rem;
    line-height: 1.6;
  }
  
  code {
    font-family: 'Monaco', 'Menlo', 'Courier New', monospace;
    background: #f0f0f0;
    padding: 0.2rem 0.4rem;
    border-radius: 4px;
    font-size: 0.9rem;
    color: #d73a49;
  }
  
  pre code {
    background: none;
    padding: 0;
    color: inherit;
  }
  
  table {
    width: 100%;
    margin: 2rem 0;
    border-collapse: separate;
    border-spacing: 0;
    background: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  }
  
  th {
    background: linear-gradient(135deg, #1FB270 0%, #17a060 100%);
    color: white;
    font-weight: 600;
    padding: 1rem 1.5rem;
    text-align: left;
    font-size: 0.95rem;
    letter-spacing: 0.5px;
  }
  
  td {
    padding: 1rem 1.5rem;
    border-top: 1px solid #e0e0e0;
    color: #666;
    font-size: 0.95rem;
    line-height: 1.6;
  }
  
  tr:hover td {
    background: #f8f9fa;
  }
  
  ul, ol {
    margin: 1.5rem 0;
    padding-left: 2rem;
    color: #666;
    line-height: 1.8;
  }
  
  li {
    margin: 0.5rem 0;
  }
  
  strong {
    font-weight: 600;
    color: #333;
  }
  
  .note-box {
    background: linear-gradient(135deg, #fff4e5 0%, #fff9f0 100%);
    border-left: 4px solid #ffa500;
    padding: 1.5rem;
    margin: 2rem 0;
    border-radius: 8px;
  }
  
  .section-divider {
    height: 2px;
    background: linear-gradient(90deg, transparent, #e0e0e0, transparent);
    margin: 4rem 0;
    border: none;
  }
  
  .step-number {
    display: inline-block;
    width: 40px;
    height: 40px;
    background: linear-gradient(135deg, #1FB270 0%, #17a060 100%);
    color: white;
    text-align: center;
    line-height: 40px;
    border-radius: 50%;
    font-weight: 600;
    font-size: 1.2rem;
    margin-right: 1rem;
  }
  
  .success-box {
    background: linear-gradient(135deg, #e7f5e7 0%, #d4f4dd 100%);
    border: 2px solid #1FB270;
    padding: 2rem;
    margin: 3rem 0;
    border-radius: 12px;
    text-align: center;
  }
  
  .success-box h2 {
    color: #1FB270;
    margin-top: 0;
    border-top: none;
    padding-top: 0;
  }
</style>

<div class="back-nav">
  <a href="../">← Back to Documentation Hub</a>
</div>

# .chat Widget Integration Guide

<p class="intro-text">
  Get the <span style="font-family: 'Raleway', sans-serif;"><span style="font-weight: 600;">Lemonflow</span><span style="font-weight: 450;">.chat</span></span> Widget running on your website or mobile application in just 3 simple steps.
</p>

<hr class="section-divider">

## <span class="step-number">1</span> Get Your Credentials

Contact our team at [tech@lemonflow.ai](mailto:tech@lemonflow.ai) to receive your unique:
- **Company ID** - Your unique identifier
- **Public Key** - Your authentication key

<div class="note-box">
  <strong>Note:</strong> Keep your credentials secure and never commit them to public repositories.
</div>

## <span class="step-number">2</span> Add the Widget Code

Place these two lines of code just before the closing `</body>` tag of your HTML page:

```html
<!-- Add this custom element where you want the widget to be anchored -->
<lemonflow-chat
    company="YOUR_COMPANY_ID"
    public-key="YOUR_PUBLIC_KEY">
</lemonflow-chat>

<!-- Add this script tag to load the widget -->
<script src="https://chat.lemonflow.ai/widget.js" async></script>
```

## <span class="step-number">3</span> Replace Your Credentials

Replace the placeholder values with your actual credentials:
- Change `YOUR_COMPANY_ID` to your company ID
- Change `YOUR_PUBLIC_KEY` to your public key

<div class="success-box">
  <h2>🎉 That's it!</h2>
  <p style="font-size: 1.1rem; color: #333; margin: 0;">
    You've successfully integrated the <strong>Lemonflow.chat</strong> widget.<br>
    Your AI assistant is now ready to help your customers 24/7.
  </p>
</div>

<hr class="section-divider">

# Advanced Configuration

For developers who want to customize the widget further or integrate with their application.

## Customization Options

You can customize the widget's appearance and behavior by adding optional attributes:

### Visual & Position Settings

| Attribute    | Description                                                    | Default          | Example Values                  |
| :----------- | :------------------------------------------------------------- | :--------------- | :------------------------------ |
| `position`   | Corner of the screen where the widget appears                 | `"bottom-right"` | `"bottom-right"`, `"bottom-left"` |
| `width`      | Width of the chat widget                                      | `"400px"`        | `"350px"`, `"50%"`              |
| `height`     | Height of the chat widget                                     | `"400px"`        | `"550px"`, `"80vh"`             |
| `z-index`    | Stack order (increase if hidden behind other elements)        | `"9999"`         | `"10000"`                       |

### Behavior Settings

| Attribute    | Description                                                    | Default          | Example Values                  |
| :----------- | :------------------------------------------------------------- | :--------------- | :------------------------------ |
| `launcher`   | Enable bubble launcher mode                                   | `"disabled"`     | `"enabled"`                     |
| `greeting`   | Text shown next to launcher bubble                            | `"Need help?"`   | `"Chat with us!"`               |
| `branding-mode` | Visual theme control                                       | `"lemonflow"`    | `"lemonflow"`, `"inherit"`      |
| `feedback-mode` | Type of feedback form after chat                           | `"health"`       | `"health"`, `"csat"`            |
| `reset`      | Show reset button for new conversations                       | `"disabled"`     | `"enabled"`                     |
| `full-screen-mode-mobile` | Full-screen on mobile devices                    | `"disabled"`     | `"enabled"`                     |

### Example: Customized Implementation

```html
<lemonflow-chat
    company="YOUR_COMPANY_ID"
    public-key="YOUR_PUBLIC_KEY"
    position="bottom-left"
    width="350px"
    height="550px"
    launcher="enabled"
    greeting="How can I help?"
    feedback-mode="csat">
</lemonflow-chat>

<script src="https://chat.lemonflow.ai/widget.js" async></script>
```

## JavaScript Integration (postMessage API)

The widget uses the standard `postMessage` API for secure communication with your application.

### Listening for Widget Events

```javascript
window.addEventListener('message', function(event) {
    // Optional: Verify origin for security
    // if (event.origin !== 'https://chat.lemonflow.ai') return;

    const data = event.data;

    switch (data.event) {
        case 'chat:ready':
            console.log('Widget initialized successfully');
            break;
            
        case 'chat:ended':
            console.log('Chat ended:', data.reason);
            // Trigger post-chat actions
            break;
            
        case 'chat:error':
            console.error('Widget error:', data.error);
            break;
            
        case 'chat:resize':
            console.log('New height:', data.height);
            // Adjust container if needed
            break;
    }
});
```

### Available Events

#### `chat:ready`
Widget successfully initialized and ready for interaction.

#### `chat:ended`
Chat session terminated.
- **`data.reason`**: String describing why the chat ended

#### `chat:error`
Critical error occurred.
- **`data.error`**: Error description

#### `chat:resize`
Widget dimensions changed.
- **`data.height`**: New height in pixels

<div class="note-box">
  <strong>Coming Soon:</strong> Sending commands to the widget (planned for v2.0.5).
</div>

## Accessibility Features

The widget is **WCAG 2.1 Level AA** compliant with comprehensive accessibility support.

### Key Features

- **Full keyboard navigation** with Tab/Shift+Tab
- **Screen reader support** with proper ARIA labels
- **Visual focus indicators** for all interactive elements
- **High contrast mode** support
- **Live regions** for dynamic content updates

### Keyboard Controls

| Key Combination | Action |
| :-------------- | :----- |
| `Tab` | Navigate forward |
| `Shift + Tab` | Navigate backward |
| `Enter` / `Space` | Activate buttons |
| `Esc` | Close widget (when launcher enabled) |

### Navigation Order

1. Reset button (if enabled)
2. Close button
3. Message input field
4. Send button

<hr class="section-divider">

<div style="text-align: center; margin-top: 4rem; padding: 2rem; background: linear-gradient(135deg, #f8f9fa 0%, #ffffff 100%); border-radius: 12px; border: 1px solid #e0e0e0;">
  <h3 style="margin-top: 0;">Need Technical Support?</h3>
  <p style="color: #666; margin-bottom: 1.5rem;">Our team is here to help with integration questions.</p>
  <a href="mailto:tech@lemonflow.ai" style="display: inline-block; padding: 0.75rem 2rem; background: linear-gradient(135deg, #1FB270 0%, #17a060 100%); color: white; text-decoration: none; border-radius: 40px; font-weight: 600; transition: all 0.3s;">Contact Support</a>
</div>