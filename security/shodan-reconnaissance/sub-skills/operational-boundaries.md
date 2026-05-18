---
name: operational-boundaries
description: Use when executing operational boundaries protocols within the security sector.
---

# Operational Boundaries: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Operational Boundaries. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Operational Boundaries

- Rate limited to 1 request per second
- Scan results not immediate (asynchronous)
- Cannot re-scan same IP within 24 hours (non-Enterprise)
- Free accounts have limited credits
- Some data requires paid subscription