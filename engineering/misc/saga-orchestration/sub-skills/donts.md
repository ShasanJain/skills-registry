---
name: donts
description: Use when executing donts protocols within the engineering sector.
---

# Donts: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Donts. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Don'ts

- **Don't assume instant completion** - Sagas take time
- **Don't skip compensation testing** - Most critical part
- **Don't couple services** - Use async messaging
- **Don't ignore partial failures** - Handle gracefully

## Resources

- [Saga Pattern](https://microservices.io/patterns/data/saga.html)
- [Designing Data-Intensive Applications](https://dataintensive.net/)