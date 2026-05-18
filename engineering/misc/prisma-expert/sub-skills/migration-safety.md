---
name: migration-safety
description: Use when executing migration safety protocols within the engineering sector.
---

# Migration Safety: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Migration Safety. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Migration Safety

- [ ] Migrations tested before production deployment
- [ ] Backward-compatible schema changes (no data loss)
- [ ] Migration scripts reviewed for correctness
- [ ] Rollback strategy documented

## Anti-Patterns to Avoid

1. **Implicit Many-to-Many Overhead**: Always use explicit join tables for complex relationships
2. **Over-Including**: Don't include relations you don't need
3. **Ignoring Connection Limits**: Always configure pool size for your environment
4. **Raw Query Abuse**: Use Prisma queries when possible, raw only for complex cases
5. **Migration in Production Dev Mode**: Never use `migrate dev` in production