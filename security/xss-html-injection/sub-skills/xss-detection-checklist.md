---
name: xss-detection-checklist
description: Use when executing xss detection checklist protocols within the security sector.
---

# Xss Detection Checklist: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Xss Detection Checklist. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# XSS Detection Checklist

```
1. Insert <script>alert(1)</script> → Check execution
2. Insert <img src=x onerror=alert(1)> → Check event handler
3. Insert "><script>alert(1)</script> → Test attribute escape
4. Insert javascript:alert(1) → Test href/src attributes
5. Check URL hash handling → DOM XSS potential
```