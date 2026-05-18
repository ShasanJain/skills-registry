---
name: no-logging
description: Use when executing no logging protocols within the ops sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core no logging logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the ops sector.

---

## 📚 Reference Material

# ❌ No Logging

## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Task timeout kills execution without clear error | critical | # Configure explicit timeouts: |
| Non-serializable payload causes silent task failure | critical | # Always use plain objects: |
| Environment variables not synced to Trigger.dev cloud | critical | # Sync env vars to Trigger.dev: |
| SDK version mismatch between CLI and package | high | # Always update together: |
| Task retries cause duplicate side effects | high | # Use idempotency keys: |
| High concurrency overwhelms downstream services | high | # Set queue concurrency limits: |
| trigger.config.ts not at project root | high | # Config must be at package root: |
| wait.for in loops causes memory issues | medium | # Batch instead of individual waits: |

## Related Skills

Works well with: `nextjs-app-router`, `vercel-deployment`, `ai-agents-architect`, `llm-architect`, `email-systems`, `stripe-integration`