---
name: not-dogfooding
description: Use when executing not dogfooding protocols within the design sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core not dogfooding logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the design sector.

---

## 📚 Reference Material

# ❌ Not Dogfooding

**Why bad**: Missing obvious UX issues.
Not finding real bugs.
Features that don't help.
No passion for improvement.

**Instead**: Use your tool daily.
Feel the pain of bad UX.
Fix what annoys YOU.
Your needs = user needs.

## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| Tool only works in your specific environment | medium | ## Making Tools Portable |
| Configuration becomes unmanageable | medium | ## Taming Configuration |
| Personal tool becomes unmaintained | low | ## Sustainable Personal Tools |
| Personal tools with security vulnerabilities | high | ## Security in Personal Tools |

## Related Skills

Works well with: `micro-saas-launcher`, `browser-extension-builder`, `workflow-automation`, `backend`