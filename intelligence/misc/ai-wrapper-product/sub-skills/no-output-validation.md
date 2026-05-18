---
name: no-output-validation
description: Use when executing no output validation protocols within the intelligence sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core no output validation logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the intelligence sector.

---

## 📚 Reference Material

# ❌ No Output Validation

**Why bad**: AI hallucinates.
Inconsistent formatting.
Bad user experience.
Trust issues.

**Instead**: Validate all outputs.
Parse structured responses.
Have fallback handling.
Post-process for consistency.

## ⚠️ Sharp Edges

| Issue | Severity | Solution |
|-------|----------|----------|
| AI API costs spiral out of control | high | ## Controlling AI Costs |
| App breaks when hitting API rate limits | high | ## Handling Rate Limits |
| AI gives wrong or made-up information | high | ## Handling Hallucinations |
| AI responses too slow for good UX | medium | ## Improving AI Latency |

## Related Skills

Works well with: `llm-architect`, `micro-saas-launcher`, `frontend`, `backend`