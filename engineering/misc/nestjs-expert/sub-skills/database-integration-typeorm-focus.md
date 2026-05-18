---
name: database-integration-typeorm-focus
description: Use when executing database integration typeorm focus protocols within the engineering sector.
---

# Database Integration Typeorm Focus: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Database Integration Typeorm Focus. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Database Integration (TypeORM Focus)

- [ ] Entity decorators use correct syntax (@Column() not @Column('description'))
- [ ] Connection errors don't crash the entire application
- [ ] Multiple database connections use named connections
- [ ] Database connections have proper error handling and retry logic
- [ ] Entities are properly registered in TypeOrmModule.forFeature()