---
name: template-5-request-for-comments-rfc-style
description: Use when executing template 5 request for comments rfc style protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core template 5 request for comments rfc style logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Template 5: Request for Comments (RFC) Style

```markdown
# RFC-0025: Adopt Event Sourcing for Order Management

## Summary

Propose adopting event sourcing pattern for the order management domain to
improve auditability, enable temporal queries, and support business analytics.

## Motivation

Current challenges:
1. Audit requirements need complete order history
2. "What was the order state at time X?" queries are impossible
3. Analytics team needs event stream for real-time dashboards
4. Order state reconstruction for customer support is manual

## Detailed Design