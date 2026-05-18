---
name: step-5-project-cash-flow
description: Use when executing step 5 project cash flow protocols within the engineering sector.
---

# Step 5 Project Cash Flow: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Step 5 Project Cash Flow. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core step 5 project cash flow logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Step 5: Project Cash Flow

Calculate monthly cash position and runway.

**Monthly Cash Flow:**
```
Beginning Cash
+ Revenue Collected (consider payment terms)
- Operating Expenses Paid
- CapEx
= Ending Cash
```

**Runway Calculation:**
```
If Ending Cash < 0:
  Funding Need = Negative Cash Balance
  Runway = 0
Else:
  Runway = Ending Cash / Average Monthly Burn
```