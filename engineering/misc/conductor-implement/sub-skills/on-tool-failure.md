---
name: on-tool-failure
description: Use when executing on tool failure protocols within the engineering sector.
---

# On Tool Failure: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing On Tool Failure. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# On Tool Failure

```
ERROR: {tool} failed with: {error message}

Options:
1. Retry the operation
2. Skip this task and continue
3. Pause implementation
4. Revert current task changes
```

- HALT and present options
- Do NOT automatically continue