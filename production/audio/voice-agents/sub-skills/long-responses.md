---
name: long-responses
description: Use when executing long responses protocols within the production sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core long responses logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the production sector.

---

## 📚 Reference Material

# ❌ Long Responses

## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Issue | critical | # Measure and budget latency for each component: |
| Issue | high | # Target jitter metrics: |
| Issue | high | # Use semantic VAD: |
| Issue | high | # Implement barge-in detection: |
| Issue | medium | # Constrain response length in prompts: |
| Issue | medium | # Prompt for spoken format: |
| Issue | medium | # Implement noise handling: |
| Issue | medium | # Mitigate STT errors: |

## Related Skills

Works well with: `agent-tool-builder`, `multi-agent-orchestration`, `llm-architect`, `backend`