---
name: no-usersession-ids
description: Use when executing no usersession ids protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core no usersession ids logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# ❌ No User/Session IDs

**Why bad**: Can't debug specific users.
Can't track sessions.
Analytics limited.

**Instead**: Always pass user_id and session_id.
Use consistent identifiers.
Add relevant metadata.

## Limitations

- Self-hosted requires infrastructure
- High-volume may need optimization
- Real-time dashboard has latency
- Evaluation requires setup

## Related Skills

Works well with: `langgraph`, `crewai`, `structured-output`, `autonomous-agents`