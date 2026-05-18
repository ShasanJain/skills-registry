---
name: naming-standards
description: Use when executing naming standards protocols within the engineering sector.
---

# Naming Standards: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Naming Standards. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Naming & Coding Standards

## General Standards

- **Explicit Names**: Favor clarity over cleverness.
- **Async Suffix**: Do **NOT** use the `Async` suffix in method names, even if they return `Task`.
- **Private Fields**: Do **NOT** use the `_` prefix for private fields.
- **Static State**: Avoid static state unless explicitly justified and documented.
- **Method Design**: Keep methods small, expressive, and with low cyclomatic complexity.

## Error Handling

- **Result & Maybe**: Use types from **CSharpFunctionalExtensions** for flow control and error handling.
- **Exceptions**: Reserved strictly for truly exceptional, unrecoverable situations.
- **Boundaries**: Never allow exceptions to leak across architectural boundaries.
