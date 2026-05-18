---
name: donts
description: Use when executing donts protocols within the engineering sector.
---

# Donts: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Donts. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Don'ts

- **Don't collect large data** - Keep data distributed
- **Don't use UDFs unnecessarily** - Use built-in functions
- **Don't over-cache** - Memory is limited
- **Don't ignore data skew** - It dominates job time
- **Don't use `.count()` for existence** - Use `.take(1)` or `.isEmpty()`

## Resources

- [Spark Performance Tuning](https://spark.apache.org/docs/latest/sql-performance-tuning.html)
- [Spark Configuration](https://spark.apache.org/docs/latest/configuration.html)
- [Databricks Optimization Guide](https://docs.databricks.com/en/optimizations/index.html)