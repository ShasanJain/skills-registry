---
name: pipeline-design
description: Use when executing pipeline design protocols within the engineering sector.
---

# Pipeline Design: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Pipeline Design. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Pipeline Design

- **Modularity**: Each stage should be independently testable
- **Idempotency**: Re-running stages should be safe
- **Observability**: Log metrics at every stage
- **Versioning**: Track data, code, and model versions
- **Failure Handling**: Implement retry logic and alerting