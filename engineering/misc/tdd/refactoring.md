---
name: refactoring
description: Use when executing refactoring protocols within the engineering sector.
---

# Refactoring: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Refactoring. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Refactor Candidates

After TDD cycle, look for:

- **Duplication** → Extract function/class
- **Long methods** → Break into private helpers (keep tests on public interface)
- **Shallow modules** → Combine or deepen
- **Feature envy** → Move logic to where data lives
- **Primitive obsession** → Introduce value objects
- **Existing code** the new code reveals as problematic
