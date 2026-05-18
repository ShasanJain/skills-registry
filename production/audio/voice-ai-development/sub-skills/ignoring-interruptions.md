---
name: ignoring-interruptions
description: Use when executing ignoring interruptions protocols within the production sector.
---

# Ignoring Interruptions: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Ignoring Interruptions. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core ignoring interruptions logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the production sector.

---

## 📚 Reference Material

# ❌ Ignoring Interruptions

**Why bad**: Frustrating user experience.
Feels like talking to a machine.
Wastes time.

**Instead**: Implement barge-in detection.
Use VAD to detect user speech.
Stop TTS immediately.
Clear audio queue.