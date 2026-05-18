---
name: single-memory-store
description: Use when executing single memory store protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core single memory store logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# ❌ Single Memory Store

## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Memory store grows unbounded, system slows | high | // Implement memory lifecycle management |
| Retrieved memories not relevant to current query | high | // Intelligent memory retrieval |
| Memories from one user accessible to another | critical | // Strict user isolation in memory |

## Related Skills

Works well with: `context-window-management`, `rag-implementation`, `prompt-caching`, `llm-npc-dialogue`