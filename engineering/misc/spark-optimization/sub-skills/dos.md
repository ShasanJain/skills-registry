---
name: dos
description: Use when executing dos protocols within the engineering sector.
---

# Dos: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Dos. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Do's

- **Enable AQE** - Adaptive query execution handles many issues
- **Use Parquet/Delta** - Columnar formats with compression
- **Broadcast small tables** - Avoid shuffle for small joins
- **Monitor Spark UI** - Check for skew, spills, GC
- **Right-size partitions** - 128MB - 256MB per partition