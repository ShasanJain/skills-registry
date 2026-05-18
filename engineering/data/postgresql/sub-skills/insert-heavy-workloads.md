---
name: insert-heavy-workloads
description: Use when executing insert heavy workloads protocols within the engineering sector.
---

# Insert Heavy Workloads: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Insert Heavy Workloads. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Insert-Heavy Workloads

- **Minimize indexes**—only create what you query; every index slows inserts.
- **Use `COPY` or multi-row `INSERT`** instead of single-row inserts.
- **UNLOGGED tables** for rebuildable staging data—much faster writes.
- **Defer index creation** for bulk loads—>drop index, load data, recreate indexes.
- **Partition by time/hash** to distribute load. **TimescaleDB** automates partitioning and compression of insert-heavy data.
- **Use a natural key for primary key** such as a (timestamp, device_id) if enforcing global uniqueness is important many insert-heavy tables don't need a primary key at all.
- If you do need a surrogate key, **Prefer `BIGINT GENERATED ALWAYS AS IDENTITY` over `UUID`**.