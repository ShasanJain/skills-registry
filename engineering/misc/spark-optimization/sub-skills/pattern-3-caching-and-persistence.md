---
name: pattern-3-caching-and-persistence
description: Use when executing pattern 3 caching and persistence protocols within the engineering sector.
---

# Pattern 3 Caching And Persistence: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Pattern 3 Caching And Persistence. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core pattern 3 caching and persistence logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Pattern 3: Caching and Persistence

```python
from pyspark import StorageLevel

# Cache when reusing DataFrame multiple times
df = spark.read.parquet("s3://bucket/data/")
df_filtered = df.filter(F.col("status") == "active")

# Cache in memory (MEMORY_AND_DISK is default)
df_filtered.cache()

# Or with specific storage level
df_filtered.persist(StorageLevel.MEMORY_AND_DISK_SER)

# Force materialization
df_filtered.count()

# Use in multiple actions
agg1 = df_filtered.groupBy("category").count()
agg2 = df_filtered.groupBy("region").sum("amount")

# Unpersist when done
df_filtered.unpersist()

# Storage levels explained:
# MEMORY_ONLY - Fast, but may not fit
# MEMORY_AND_DISK - Spills to disk if needed (recommended)
# MEMORY_ONLY_SER - Serialized, less memory, more CPU
# DISK_ONLY - When memory is tight
# OFF_HEAP - Tungsten off-heap memory

# Checkpoint for complex lineage
spark.sparkContext.setCheckpointDir("s3://bucket/checkpoints/")
df_complex = (df
    .join(other_df, "key")
    .groupBy("category")
    .agg(F.sum("amount")))
df_complex.checkpoint()  # Breaks lineage, materializes
```