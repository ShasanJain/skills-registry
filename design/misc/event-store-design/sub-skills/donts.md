---
name: donts
description: Use when executing donts protocols within the design sector.
---

# Donts: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Donts. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Don'ts

- **Don't update or delete events** - They're immutable facts
- **Don't store large payloads** - Keep events small
- **Don't skip optimistic concurrency** - Prevents data corruption
- **Don't ignore backpressure** - Handle slow consumers

## Resources

- [EventStoreDB](https://www.eventstore.com/)
- [Marten Events](https://martendb.io/events/)
- [Event Sourcing Pattern](https://docs.microsoft.com/en-us/azure/architecture/patterns/event-sourcing)