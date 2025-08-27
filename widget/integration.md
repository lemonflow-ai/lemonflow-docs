---
title: .chat (widget)
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
  
  h2:first-child {
    border-top: none;
    padding-top: 0;
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
    font-size: 0.85rem;
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
</style>


<h1 style="margin: 3rem 0 1.5rem 0;">
  <span style="display: block; font-size: 2.5rem; font-weight: 700; background: linear-gradient(135deg, #1FB270 0%, #8fd3f4 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">Integration Guide</span>
  <span style="display: block; font-size: 1.8rem; color: #333; font-weight: 600; margin-top: 0.5rem;">.chat Widget</span>
</h1>

<p class="intro-text">
  This guide provides everything you need to integrate the Lemonflow.chat Widget into your website or mobile application with just two lines of code.
</p>

## 1. Basic Integration

To add the chat widget to your website or mobile application, place the following two lines of code just before the closing `</body>` tag of your HTML page.

```html
<!-- Add this custom element where you want the widget to be anchored -->
<lemonflow-chat
    company="YOUR_COMPANY_ID"
    public-key="YOUR_PUBLIC_KEY">
</lemonflow-chat>

<!-- Add this script tag to load the widget -->
<script src="https://chat.lemonflow.ai/widget.js" async></script>
```

<div class="note-box">
  <strong>Important:</strong> Replace <code>YOUR_COMPANY_ID</code> and <code>YOUR_PUBLIC_KEY</code> with the credentials provided to you by Lemonflow.
</div>

## 2. Customization Options

You can customize the widget's appearance by adding attributes to the `<lemonflow-chat>` element. 

### Available Attributes

| Attribute    | Description                                                                 | Default          | Example Values                  |
| :----------- | :-------------------------------------------------------------------------- | :--------------- | :------------------------------ |
| `company`    | **Required** - Your unique company identifier                               | -                | `"my-company"`                  |
| `public-key` | **Required** - Your public API key for authentication                       | -                | `"pk_lemonflow_..."`            |
| `position`   | Corner of the screen where the widget will be fixed                         | `"bottom-right"` | `"bottom-right"`, `"bottom-left"` |
| `width`      | Width of the chat widget                                                    | `"400px"`        | `"350px"`, `"50%"`              |
| `height`     | Height of the chat widget                                                   | `"400px"`        | `"550px"`, `"80vh"`             |
| `z-index`    | Stack order of the widget (increase if hidden behind content)               | `"9999"`         | `"10000"`                       |
| `launcher`   | Enables bubble launcher mode                                                | disabled         | `"enabled"`                     |
| `greeting`   | Text displayed next to the launcher bubble                                  | `"Need help?"`   | `"Chat with us!"`               |
| `branding-mode` | Controls the widget's visual theme                                       | `"lemonflow"`    | `"lemonflow"`, `"inherit"`      |
| `feedback-mode` | Type of feedback form displayed after chat                               | `"health"`       | `"health"`, `"csat"`            |
| `reset`         | Shows reset button to start new conversations                            | `"disabled"`     | `"enabled"`, `"disabled"`       |
| `full-screen-mode-mobile` | Enables full-screen mode on mobile devices                     | `"disabled"`     | `"enabled"`, `"disabled"`       |

### Example: Customized Widget

This example places a smaller widget in the bottom-left corner, enables the launcher, and sets the feedback mode to CSAT.

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

<div style="background: linear-gradient(135deg, #e7f5e7 0%, #d4f4dd 100%); border: 2px solid #1FB270; padding: 2rem; margin: 3rem 0; border-radius: 12px; text-align: center;">
  <h2 style="color: #1FB270; margin-top: 0; border-top: none; padding-top: 0; font-size: 1.8rem;">🎉 That's it!</h2>
  <p style="font-size: 1.1rem; color: #333; margin: 0; line-height: 1.6;">
    You've successfully integrated the <strong>Lemonflow.chat</strong> widget.<br>
    Your AI assistant is now ready to help your customers 24/7.
  </p>
</div>

# Advanced Developer Options

## 3. JavaScript Integration (postMessage API)

The widget communicates with your host page using the standard `postMessage` API, allowing for secure, event-driven integration.

### Listening for Events from the Widget

You can listen for events to understand the widget's state and respond accordingly.

```javascript
window.addEventListener('message', function(event) {
    // Optional: Add a security check for the origin
    // if (event.origin !== 'https://chat.lemonflow.ai') {
    //     return;
    // }

    const data = event.data;

    switch (data.event) {
        case 'chat:ready':
            console.log('Lemonflow Chat is ready!');
            break;
        case 'chat:ended':
            console.log('Chat session ended. Reason:', data.reason);
            // Example: Trigger a survey or other follow-up action
            break;
        case 'chat:error':
            console.error('An error occurred in the chat widget:', data.error);
            break;
        case 'chat:resize':
            console.log('Chat resized. New height:', data.height);
            // Example: Adjust the iframe height dynamically
            const iframe = document.getElementById('lemonflow-chat-iframe');
            if (iframe && data.height) {
                iframe.style.height = `${data.height}px`;
            }
            break;
    }
});
```

### Events Sent by the Widget

| Event | Description | Data Properties |
| :---- | :---------- | :-------------- |
| `chat:ready` | Widget successfully initialized and ready to accept messages | - |
| `chat:ended` | Chat session terminated by user, agent, or timeout | `data.reason` (string): Why the chat ended |
| `chat:error` | Critical error occurred within the widget | `data.error` (string): Error description |
| `chat:resize` | Internal content height changed | `data.height` (number): New height in pixels |

<div class="note-box">
  <strong>Coming Soon:</strong> Sending commands to the widget is planned for v2.0.5 and is not yet available.
</div>

## 4. Accessibility Features

The <span style="font-family: 'Raleway', sans-serif;"><span style="font-weight: 600;">Lemonflow</span><span style="font-weight: 450;">.ai</span></span> Chat Widget is designed to be accessible and compliant with **WCAG 2.1 Level AA** standards.

### Key Accessibility Features

- **Keyboard Navigation**: All interactive elements accessible via Tab key and activated with Enter/Space
- **Screen Reader Support**: Proper ARIA labels and roles for assistive technologies  
- **Focus Management**: Clear visual focus indicators for keyboard users
- **Alternative Text**: Descriptive labels for icons and images
- **Live Regions**: Screen readers announce new messages and status changes

### Keyboard Navigation Guide

To activate keyboard mode:

1. **Click anywhere on the chat widget** to bring it into focus
2. **Press Tab** to start navigating through interactive elements

#### Navigation Flow

When pressing Tab, focus moves through elements in this order:

1. **Reset button** (↻ icon) - if enabled
2. **Close button** (× icon)
3. **Message input field** ("Type your message...")  
4. **Send button**

#### Keyboard Controls

| Key | Action |
| :--- | :----- |
| **Tab** | Move forward through interactive elements |
| **Shift + Tab** | Move backward through elements |
| **Enter** | Activate the currently focused button |
| **Space** | Activate buttons (alternative to Enter) |
| **Type directly** | When input field is focused, start typing your message |

#### Visual Focus Indicators

- **Active focus**: Black outline appears around the currently focused element
- **Clear feedback**: Each interactive element displays a prominent black border when focused
- **Consistent styling**: Focus indicators maintain the same appearance across all elements

### High Contrast Support

The widget automatically adapts to system high contrast settings and maintains sufficient color contrast ratios for all text and interactive elements, ensuring readability for users with visual impairments.