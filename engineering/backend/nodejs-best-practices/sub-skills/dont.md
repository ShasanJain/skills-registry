---
name: dont
description: Use when executing dont protocols within the engineering sector.
---

# Dont: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Dont. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# ❌ DON'T:

- Use Express for new edge projects (use Hono)
- Use sync methods in production code
- Put business logic in controllers
- Skip input validation
- Hardcode secrets
- Trust external data without validation
- Block event loop with CPU work