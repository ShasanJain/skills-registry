---
name: workflows-orchestration
description: Use when executing workflows orchestration protocols within the ops sector.
---

# Workflows Orchestration: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Workflows Orchestration. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Workflows (Orchestration)

**Characteristics:**

- Contain business logic and coordination
- **MUST be deterministic** (same inputs → same outputs)
- **Cannot** perform direct external calls
- State automatically preserved across failures
- Can run for years despite infrastructure failures

**Example workflow tasks:**

- Decide which steps to execute
- Handle compensation logic
- Manage timeouts and retries
- Coordinate child workflows