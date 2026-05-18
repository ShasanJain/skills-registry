---
name: blocking-the-event-loop
description: Use when executing blocking the event loop protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core blocking the event loop logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# ❌ Blocking the Event Loop

**Why bad**: Discord gateway requires regular heartbeats. Blocking operations
cause missed heartbeats and disconnections.

## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Issue | critical | ## Acknowledge immediately, process later |
| Issue | critical | ## Step 1: Enable in Developer Portal |
| Issue | high | ## Use a separate deploy script (not on startup) |
| Issue | critical | ## Never hardcode tokens |
| Issue | high | ## Generate correct invite URL |
| Issue | medium | ## Development: Use guild commands |
| Issue | medium | ## Never block the event loop |
| Issue | medium | ## Show modal immediately |