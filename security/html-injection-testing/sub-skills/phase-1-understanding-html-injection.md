---
name: phase-1-understanding-html-injection
description: Use when executing phase 1 understanding html injection protocols within the security sector.
---

# Phase 1 Understanding Html Injection: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 1 Understanding Html Injection. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Phase 1: Understanding HTML Injection

HTML injection occurs when user input is reflected in web pages without proper sanitization:

```html
<!-- Vulnerable code example -->
<div>
    Welcome, <?php echo $_GET['name']; ?>
</div>

<!-- Attack input -->
?name=<h1>Injected Content</h1>

<!-- Rendered output -->
<div>
    Welcome, <h1>Injected Content</h1>
</div>
```

Key differences from XSS:
- HTML injection: Only HTML tags are rendered
- XSS: JavaScript code is executed
- HTML injection is often stepping stone to XSS

Attack goals:
- Modify website appearance (defacement)
- Create fake login forms (phishing)
- Inject malicious links
- Display misleading content