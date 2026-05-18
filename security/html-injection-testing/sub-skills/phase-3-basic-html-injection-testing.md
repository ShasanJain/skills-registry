---
name: phase-3-basic-html-injection-testing
description: Use when executing phase 3 basic html injection testing protocols within the security sector.
---

# Phase 3 Basic Html Injection Testing: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 3 Basic Html Injection Testing. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 3 basic html injection testing logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Phase 3: Basic HTML Injection Testing

Test with simple HTML tags:

```html
<!-- Basic text formatting -->
<h1>Test Injection</h1>
<b>Bold Text</b>
<i>Italic Text</i>
<u>Underlined Text</u>
<font color="red">Red Text</font>

<!-- Structural elements -->
<div style="background:red;color:white;padding:10px">Injected DIV</div>
<p>Injected paragraph</p>
<br><br><br>Line breaks

<!-- Links -->
<a href="http://attacker.com">Click Here</a>
<a href="http://attacker.com">Legitimate Link</a>

<!-- Images -->
<img src="http://attacker.com/image.png">
<img src="x" onerror="alert(1)">  <!-- XSS attempt -->
```

Testing workflow:
```bash
# Test basic injection
curl "http://target.com/search?q=<h1>Test</h1>"

# Check if HTML renders in response
curl -s "http://target.com/search?q=<b>Bold</b>" | grep -i "bold"

# Test in URL-encoded form
curl "http://target.com/search?q=%3Ch1%3ETest%3C%2Fh1%3E"
```