---
name: 2-flaky-integration-test
description: Use when executing 2 flaky integration test protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 2 flaky integration test logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 2. Flaky Integration Test

**Issue**: `test_payment_flow` fails intermittently in CI
**Workaround**: Re-run failed job (usually passes on retry)
**Ticket**: ENG-1200 (P2)

---

## 📅 Upcoming Events

| Date | Event | Impact | Contact |
|------|-------|--------|---------|
| 01/23 02:00 | Database maintenance | 5 min read-only | @dba-team |
| 01/24 14:00 | Major release v5.0 | Monitor closely | @release-team |
| 01/25 | Marketing campaign | 2x traffic expected | @platform |

---

## 📞 Escalation Reminders

| Issue Type | First Escalation | Second Escalation |
|------------|------------------|-------------------|
| Payment issues | @payments-oncall | @payments-manager |
| Auth issues | @auth-oncall | @security-team |
| Database issues | @dba-team | @infra-manager |
| Unknown/severe | @engineering-manager | @vp-engineering |

---

## 🔧 Quick Reference