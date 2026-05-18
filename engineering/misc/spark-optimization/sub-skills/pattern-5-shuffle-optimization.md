---
name: pattern-5-shuffle-optimization
description: Use when executing pattern 5 shuffle optimization protocols within the engineering sector.
---

# Pattern 5 Shuffle Optimization: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Pattern 5 Shuffle Optimization. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core pattern 5 shuffle optimization logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Pattern 5: Shuffle Optimization

```python
# Reduce shuffle data size
spark.conf.set("spark.sql.shuffle.partitions", "auto")  # With AQE
spark.conf.set("spark.shuffle.compress", "true")
spark.conf.set("spark.shuffle.spill.compress", "true")

# Pre-aggregate before shuffle
df_optimized = (df
    # Local aggregation first (combiner)
    .groupBy("key", "partition_col")
    .agg(F.sum("value").alias("partial_sum"))
    # Then global aggregation
    .groupBy("key")
    .agg(F.sum("partial_sum").alias("total")))

# Avoid shuffle with map-side operations
# BAD: Shuffle for each distinct
distinct_count = df.select("category").distinct().count()

# GOOD: Approximate distinct (no shuffle)
approx_count = df.select(F.approx_count_distinct("category")).collect()[0][0]

# Use coalesce instead of repartition when reducing partitions
df_reduced = df.coalesce(10)  # No shuffle

# Optimize shuffle with compression
spark.conf.set("spark.io.compression.codec", "lz4")  # Fast compression
```