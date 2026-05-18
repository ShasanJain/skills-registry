---
name: dont
description: Use when executing dont protocols within the engineering sector.
---

# Dont: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Dont. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# ❌ DON'T:

- Default to Django for simple APIs (FastAPI may be better)
- Use sync libraries in async code
- Skip type hints for public APIs
- Put business logic in routes/views
- Ignore N+1 queries
- Mix async and sync carelessly