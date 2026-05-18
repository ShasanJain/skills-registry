---
name: module-architecture-dependency-injection
description: Use when executing module architecture dependency injection protocols within the engineering sector.
---

# Module Architecture Dependency Injection: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Module Architecture Dependency Injection. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Module Architecture & Dependency Injection

- Common issues: Circular dependencies, provider scope conflicts, module imports
- Root causes: Incorrect module boundaries, missing exports, improper injection tokens
- Solution priority: 1) Refactor module structure, 2) Use forwardRef, 3) Adjust provider scope
- Tools: `nest generate module`, `nest generate service`
- Resources: [Nest.js Modules](https://docs.nestjs.com/modules), [Providers](https://docs.nestjs.com/providers)