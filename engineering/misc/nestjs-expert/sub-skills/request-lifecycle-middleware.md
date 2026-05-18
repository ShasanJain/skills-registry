---
name: request-lifecycle-middleware
description: Use when executing request lifecycle middleware protocols within the engineering sector.
---

# Request Lifecycle Middleware: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Request Lifecycle Middleware. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Request Lifecycle & Middleware

- [ ] Middleware execution order follows: Middleware → Guards → Interceptors → Pipes
- [ ] Guards properly protect routes and return boolean/throw exceptions
- [ ] Interceptors handle async operations correctly
- [ ] Exception filters catch and transform errors appropriately
- [ ] Pipes validate DTOs with class-validator decorators