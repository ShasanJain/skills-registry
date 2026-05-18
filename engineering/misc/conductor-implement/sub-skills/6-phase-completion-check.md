---
name: 6-phase-completion-check
description: Use when executing 6 phase completion check protocols within the engineering sector.
---

# 6 Phase Completion Check: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 6 Phase Completion Check. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 6. Phase Completion Check

After each task, check if phase is complete:

- Parse plan.md for phase structure
- If all tasks in current phase are `[x]`:

**Run phase verification:**

```
Phase {N} complete. Running verification...
```

- Execute verification tasks listed for the phase
- Run full test suite: `npm test` / `pytest` / etc.

**Report and wait for approval:**

```
Phase {N} Verification Results:
- All phase tasks: Complete
- Tests: {passing/failing}
- Verification: {pass/fail}

Approve to continue to Phase {N+1}?
1. Yes, continue
2. No, there are issues to fix
3. Pause implementation
```

**CRITICAL: Wait for explicit user approval before proceeding to next phase.**

## Error Handling During Implementation