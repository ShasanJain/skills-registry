---
name: not-flushing-in-serverless
description: Use when executing not flushing in serverless protocols within the engineering sector.
---

# Not Flushing In Serverless: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Not Flushing In Serverless. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core not flushing in serverless logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# ❌ Not Flushing in Serverless

**Why bad**: Traces are batched.
Serverless may exit before flush.
Data is lost.

**Instead**: Always call langfuse.flush() at end.
Use context managers where available.
Consider sync mode for critical traces.