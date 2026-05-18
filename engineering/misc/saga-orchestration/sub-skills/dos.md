---
name: dos
description: Use when executing dos protocols within the engineering sector.
---

# Dos: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Dos. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Do's

- **Make steps idempotent** - Safe to retry
- **Design compensations carefully** - They must work
- **Use correlation IDs** - For tracing across services
- **Implement timeouts** - Don't wait forever
- **Log everything** - For debugging failures