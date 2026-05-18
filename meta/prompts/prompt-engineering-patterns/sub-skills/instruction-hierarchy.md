---
name: instruction-hierarchy
description: Use when applying instruction hierarchy patterns to optimize agent workflows and prompts.
---

# Instruction Hierarchy: Operational Execution SOP

## ⚙️ Overview
This protocol defines the strict standard for implementing Instruction Hierarchy. By following this SOP, the engine ensures token efficiency, maximum architectural stability, and robust caching.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the pattern:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like TS, ESLint, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core instruction hierarchy logic into the active code or prompt block.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs.

---

## 📚 Reference Material

# Instruction Hierarchy

```
[System Context] → [Task Instruction] → [Examples] → [Input Data] → [Output Format]
```
