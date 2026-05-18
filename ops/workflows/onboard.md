# Onboard: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Onboard. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core onboard logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the ops sector.

---

## 📚 Reference Material

---
description: Người mới vào team? Hướng dẫn họ tự động.
---

# /onboard - Team Onboarding

$ARGUMENTS

---

## Task
Help a new developer join the project efficiently.

### Steps:
1.  **Explain Architecture**: Summarize `ARCHITECTURE.md` (or `.vi.md`).
2.  **Environment Setup**: Check `.env` and dependencies.
3.  **Run Project**: Guide through `npm run dev`.
4.  **First Task**: Suggest a "Good First Issue" to fix.

---

## Usage
```
/onboard        # Start interactive guide
/onboard docs   # Show key documentation links
```
