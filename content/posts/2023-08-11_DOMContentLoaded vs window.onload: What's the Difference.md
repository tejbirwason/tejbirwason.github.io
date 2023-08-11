---
title: "DOMContentLoaded vs window.onload What's the Difference"
date: 2023-08-11
---

When building web pages, it's important to know when to execute JavaScript. Two crucial events, `DOMContentLoaded` and `window.onload`, can help you determine this. Let's explore the differences.

## Timing

- **DOMContentLoaded**: Fires when the HTML document is fully parsed. The DOM is ready, but resources like images might not be loaded yet.
- **window.onload**: Fires when the entire page, including all resources (images, stylesheets, etc.), is fully loaded.

## Use Cases

- **DOMContentLoaded**: Ideal for running JavaScript as soon as the DOM is ready, without waiting for all resources. This ensures a faster user experience.
- **window.onload**: Perfect when your script needs every resource, like images, to be loaded.

## Adding Event Listeners

- **DOMContentLoaded**:
  ```javascript
  document.addEventListener('DOMContentLoaded', function () {
    // Your code here
  });
  ```
- **window.onload**:
  ```javascript
  window.onload = function () {
    // Your code here
  };
  ```

## Performance

Using `window.onload` might delay your JavaScript, especially with many large resources on a page. If all resources aren't essential for your script, `DOMContentLoaded` usually offers better perceived performance.

## Browser Support

- **DOMContentLoaded**: Supported by modern browsers but not by IE versions less than 9.
- **window.onload**: Has extensive backward compatibility across browsers.

**Conclusion**: Choose between `DOMContentLoaded` and `window.onload` based on when you need your JavaScript to run. If it's just the DOM, use `DOMContentLoaded`. If it's every resource, use `window.onload`.
