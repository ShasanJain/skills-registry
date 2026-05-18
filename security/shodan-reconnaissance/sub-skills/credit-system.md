---
name: credit-system
description: Use when executing credit system protocols within the security sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core credit system logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the security sector.

---

## 📚 Reference Material

# Credit System

| Action | Credit Type | Cost |
|--------|-------------|------|
| Basic search | Query | 0 (no filters) |
| Filtered search | Query | 1 |
| Download 100 results | Query | 1 |
| Generate report | Query | 1 |
| Scan 1 IP | Scan | 1 |
| Network monitoring | Monitored IPs | Depends on plan |

## Constraints and Limitations