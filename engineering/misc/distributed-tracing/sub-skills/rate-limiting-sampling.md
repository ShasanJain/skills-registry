---
name: rate-limiting-sampling
description: Use when executing rate limiting sampling protocols within the engineering sector.
---

# Rate Limiting Sampling: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Rate Limiting Sampling. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core rate limiting sampling logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Rate Limiting Sampling

```yaml
# Sample max 100 traces per second
sampler:
  type: ratelimiting
  param: 100
```