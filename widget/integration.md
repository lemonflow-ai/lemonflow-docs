---
title: 🍋 Chat Widget Integration Guide
---

<div style="background: #f8f9fa; padding: 0.5rem 1rem; margin-bottom: 1rem; border-radius: 4px; font-size: 0.9rem;">
  <a href="../">← Back to Documentation Hub</a>
</div>

This guide provides everything you need to integrate the Lemonflow Chat Widget into your website.

## 1. Basic Integration

To add the chat widget to your site, place the following two lines of code just before the closing `</body>` tag of your HTML page.

```html
<!-- Add this custom element where you want the widget to be anchored -->
<lemonflow-chat
    company="YOUR_COMPANY_ID"
    public-key="YOUR_PUBLIC_KEY">
</lemonflow-chat>

<!-- Add this script tag to load the widget -->
<script src="https://staging-chat-57182386284.europe-west4.run.app/widget.js" async></script>
```

-   Replace `YOUR_COMPANY_ID` and `YOUR_PUBLIC_KEY` with the credentials provided to you by Lemonflow.

## 2. Customization

You can customize the widget's appearance and position by adding attributes to the `<lemonflow-chat>` element.

| Attribute    | Description                                                                 | Default          | Example Values                  |
| :----------- | :-------------------------------------------------------------------------- | :--------------- | :------------------------------ |
| `company`    | **(Required)** Your unique company identifier.                              | -                | `"my-company"`                  |
| `public-key` | **(Required)** Your public API key for authentication.                      | -                | `"pk_lemonflow_..."`            |
| `position`   | The corner of the screen where the widget will be fixed.                    | `"bottom-right"` | `"bottom-right"`, `"bottom-left"` |
| `width`      | The width of the chat widget.                                               | `"400px"`        | `"350px"`, `"50%"`                |
| `height`     | The height of the chat widget.                                              | `"400px"`        | `"550px"`, `"80vh"`               |
| `z-index`    | The stack order of the widget. Increase if it's hidden behind other content. | `"9999"`         | `"10000"`                       |
| `launcher`   | Enables the bubble launcher mode.                                           | (disabled)       | `"enabled"`                     |
| `greeting`   | The text displayed next to the launcher bubble.                             | `"Need help?"`   | `"Chat with us!"`               |
| `branding-mode` | Controls the widget's visual theme.                                       | `"lemonflow"`    | `"lemonflow"`, `"inherit"`      |
| `feedback-mode` | The type of feedback form to display after a chat.                        | `"health"`       | `"health"`, `"csat"`            |
| `reset`         | Shows a reset button to start new conversations.                          | `"disabled"`     | `"enabled"`, `"disabled"`       |
| `full-screen-mode-mobile` | Enables full-screen mode on mobile devices.                     | `"disabled"`     | `"enabled"`, `"disabled"`       |

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
```

## 3. Interacting with the Widget (`postMessage` API)

The widget communicates with your host page using the standard `postMessage` API, allowing for a secure, event-driven integration.

### Listening for Events from the Widget

You can listen for events to understand the widget's state.

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
            const iframe = document.getElementById('lemonflow-chat-iframe'); // Make sure your iframe has an ID
            if (iframe && data.height) {
                iframe.style.height = `${data.height}px`;
            }
            break;
    }
});
```

#### Events Sent by the Widget

-   **`chat:ready`**: Fired when the widget has successfully initialized and is ready to accept messages.
-   **`chat:ended`**: Fired when the chat session is terminated by the user, agent, or inactivity timeout.
    -   `data.reason` (string): A brief description of why the chat ended.
-   **`chat:error`**: Fired if a critical error occurs within the widget.
    -   `data.error` (string): A description of the error.
-   **`chat:resize`**: Fired whenever the internal content height of the chat changes. This allows the parent page to dynamically adjust the iframe's height to prevent scrollbars or empty space.
    -   `data.height` (number): The new required height in pixels.

### Sending Commands to the Widget

*This functionality is planned for a future release (v2.0.5) and is not yet active.*

## 5. Accessibility

The Lemonflow Chat Widget is designed to be accessible and compliant with **WCAG 2.1 Level AA** standards.

### Accessibility Features

- **Keyboard Navigation**: All interactive elements can be accessed using the Tab key and activated with Enter/Space
- **Screen Reader Support**: Proper ARIA labels and roles for assistive technologies
- **Focus Management**: Clear visual focus indicators for keyboard users
- **Alternative Text**: Descriptive labels for icons and images
- **Live Regions**: Screen readers announce new messages and status changes

### Keyboard Navigation

The widget provides full keyboard navigation support. To activate keyboard mode:

1. **Click anywhere on the chat widget** to bring it into focus
2. **Press Tab** to start navigating through interactive elements

#### Navigation Flow

When pressing Tab, focus moves through elements in this order:
1. **Reset button** (↻ icon) - if enabled
2. **Close button** (× icon) 
3. **Message input field** ("Type your message...")
4. **Send button**

#### Visual Focus Indicators

- **Active focus indicator**: Black outline appears around the currently focused element
- **Clear visual feedback**: Each interactive element displays a prominent black border when focused
- **Consistent styling**: Focus indicators maintain the same appearance across all elements

#### Keyboard Controls

- **Tab**: Move forward through interactive elements
- **Shift + Tab**: Move backward through elements  
- **Enter**: Activate the currently focused button
- **Space**: Activate buttons (alternative to Enter)
- **Type directly**: When input field is focused, start typing your message

### High Contrast Support

The widget adapts to system high contrast settings and provides sufficient color contrast ratios for all text and interactive elements.