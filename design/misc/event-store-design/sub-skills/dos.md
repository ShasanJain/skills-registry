---
name: dos
description: Use when executing dos protocols within the design sector.
---

# Dos: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Dos. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Do's

- **Use stream IDs that include aggregate type** - `Order-{uuid}`
- **Include correlation/causation IDs** - For tracing
- **Version events from day one** - Plan for schema evolution
- **Implement idempotency** - Use event IDs for deduplication
- **Index appropriately** - For your query patterns