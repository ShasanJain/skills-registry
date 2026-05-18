---
name: testing-mocking
description: Use when executing testing mocking protocols within the engineering sector.
---

# Testing Mocking: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Testing Mocking. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Testing & Mocking

- [ ] Test modules use minimal, focused provider mocks
- [ ] TypeORM repositories use getRepositoryToken(Entity) for mocking
- [ ] No actual database dependencies in unit tests
- [ ] All async operations are properly awaited in tests
- [ ] JwtService and external dependencies are mocked appropriately