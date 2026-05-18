---
name: schema-quality
description: Use when executing schema quality protocols within the engineering sector.
---

# Schema Quality: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Schema Quality. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Schema Quality

- [ ] All models have appropriate `@id` and primary keys
- [ ] Relations use explicit `@relation` with `fields` and `references`
- [ ] Cascade behaviors defined (`onDelete`, `onUpdate`)
- [ ] Indexes added for frequently queried fields
- [ ] Enums used for fixed value sets
- [ ] `@@map` used for table naming conventions