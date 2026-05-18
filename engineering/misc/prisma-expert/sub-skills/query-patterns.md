---
name: query-patterns
description: Use when executing query patterns protocols within the engineering sector.
---

# Query Patterns: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Query Patterns. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Query Patterns

- [ ] No N+1 queries (relations included when needed)
- [ ] `select` used to fetch only required fields
- [ ] Pagination implemented for list queries
- [ ] Raw queries used for complex aggregations
- [ ] Proper error handling for database operations