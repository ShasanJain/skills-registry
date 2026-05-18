---
name: middleware-guards-interceptors-pipes
description: Use when executing middleware guards interceptors pipes protocols within the engineering sector.
---

# Middleware Guards Interceptors Pipes: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Middleware Guards Interceptors Pipes. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Middleware, Guards, Interceptors & Pipes

- Common issues: Execution order, context access, async operations
- Root causes: Incorrect implementation, missing async/await, improper error handling
- Solution priority: 1) Fix execution order, 2) Handle async properly, 3) Implement error handling
- Execution order: Middleware → Guards → Interceptors (before) → Pipes → Route handler → Interceptors (after)
- Resources: [Middleware](https://docs.nestjs.com/middleware), [Guards](https://docs.nestjs.com/guards)