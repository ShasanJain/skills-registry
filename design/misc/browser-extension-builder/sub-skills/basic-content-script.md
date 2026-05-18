---
name: basic-content-script
description: Use when executing basic content script protocols within the design sector.
---

# Basic Content Script: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Basic Content Script. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core basic content script logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the design sector.

---

## 📚 Reference Material

# Basic Content Script

```javascript
// content.js - Runs on every matched page

// Wait for page to load
document.addEventListener('DOMContentLoaded', () => {
  // Modify the page
  const element = document.querySelector('.target');
  if (element) {
    element.style.backgroundColor = 'yellow';
  }
});

// Listen for messages from popup/background
chrome.runtime.onMessage.addListener((message, sender, sendResponse) => {
  if (message.action === 'getData') {
    const data = document.querySelector('.data')?.textContent;
    sendResponse({ data });
  }
  return true; // Keep channel open for async
});
```