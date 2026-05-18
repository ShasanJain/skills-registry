---
name: equity-pool-sizing
description: Use when executing equity pool sizing protocols within the engineering sector.
---

# Equity Pool Sizing: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Equity Pool Sizing. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core equity pool sizing logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Equity Pool Sizing

**Option Pool by Round:**
- Pre-Seed: 10-15% reserved
- Seed: 10-15% top-up
- Series A: 10-15% top-up
- Series B+: 5-10% per round

**Pre-Funding Dilution:**
Investors often require option pool creation before investment, diluting founders.

**Example:**
```
Pre-money: $10M
Investors want 15% option pool post-money

Calculation:
Post-money: $15M ($10M + $5M investment)
Option pool: $2.25M (15% × $15M)
Founders diluted by pool creation before new money
```

## Organizational Design