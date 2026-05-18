---
name: data-integration-patterns
description: Use when executing data integration patterns protocols within the engineering sector.
---

# Data Integration Patterns: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Data Integration Patterns. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Data Integration Patterns

- **Data access layer**: Repository pattern, DAO pattern, unit of work
- **ORM integration**: Entity Framework, SQLAlchemy, Prisma, TypeORM
- **Database per service**: Service autonomy, data ownership, eventual consistency
- **Shared database**: Anti-pattern considerations, legacy integration
- **API composition**: Data aggregation, parallel queries, response merging
- **CQRS integration**: Command models, query models, read replicas
- **Event-driven data sync**: Change data capture, event propagation
- **Database transaction management**: ACID, distributed transactions, sagas
- **Connection pooling**: Pool sizing, connection lifecycle, cloud considerations
- **Data consistency**: Strong vs eventual consistency, CAP theorem trade-offs