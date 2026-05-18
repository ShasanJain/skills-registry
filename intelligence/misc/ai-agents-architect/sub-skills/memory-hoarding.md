---
name: memory-hoarding
description: Use when executing memory hoarding protocols within the intelligence sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core memory hoarding logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the intelligence sector.

---

## 📚 Reference Material

# ❌ Memory Hoarding

## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Agent loops without iteration limits | critical | Always set limits: |
| Vague or incomplete tool descriptions | high | Write complete tool specs: |
| Tool errors not surfaced to agent | high | Explicit error handling: |
| Storing everything in agent memory | medium | Selective memory: |
| Agent has too many tools | medium | Curate tools per task: |
| Using multiple agents when one would work | medium | Justify multi-agent: |
| Agent internals not logged or traceable | medium | Implement tracing: |
| Fragile parsing of agent outputs | medium | Robust output handling: |

## Related Skills

Works well with: `rag-engineer`, `prompt-engineer`, `backend`, `mcp-builder`