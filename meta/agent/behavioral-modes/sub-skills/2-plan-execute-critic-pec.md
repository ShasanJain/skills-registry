---
name: 2-plan-execute-critic-pec
description: Use when applying 2 plan execute critic pec patterns to optimize agent workflows.
---

# 2 Plan Execute Critic Pec: Standard Operating Procedure

## ⚙️ Overview
This protocol defines the strict standard for implementing 2 Plan Execute Critic Pec. By following this SOP, the engine ensures token efficiency, maximum architectural stability, robust caching, and adherence to all operational guardrails established by the system architecture.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the pattern:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like TS, ESLint, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 2 plan execute critic pec logic into the active code or prompt block.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs.

---

## 📚 Reference Material

# 2. 🗺️ PLAN-EXECUTE-CRITIC (PEC)

Cyclic mode transitions for high-complexity tasks:
1. **Planner:** Decomposes the task into atomic steps (`task.md`).
2. **Executor:** Performs the actual coding (`IMPLEMENT`).
3. **Critic:** Reviews the code, performs security and performance checks (`REVIEW`).