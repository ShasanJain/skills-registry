---
name: on-git-failure
description: Use when executing on git failure protocols within the engineering sector.
---

# On Git Failure: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing On Git Failure. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# On Git Failure

```
GIT ERROR: {error message}

This may indicate:
- Uncommitted changes from outside Conductor
- Merge conflicts
- Permission issues

Options:
1. Show git status
2. Attempt to resolve
3. Pause for manual intervention
```

## Track Completion

When all phases and tasks are complete: