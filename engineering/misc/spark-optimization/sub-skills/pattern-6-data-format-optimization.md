---
name: pattern-6-data-format-optimization
description: Use when executing pattern 6 data format optimization protocols within the engineering sector.
---

# Pattern 6 Data Format Optimization: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Pattern 6 Data Format Optimization. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core pattern 6 data format optimization logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Pattern 6: Data Format Optimization

```python
# Parquet optimizations
(df.write
    .option("compression", "snappy")  # Fast compression
    .option("parquet.block.size", 128 * 1024 * 1024)  # 128MB row groups
    .parquet("s3://bucket/output/"))

# Column pruning - only read needed columns
df = (spark.read.parquet("s3://bucket/data/")
    .select("id", "amount", "date"))  # Spark only reads these columns

# Predicate pushdown - filter at storage level
df = (spark.read.parquet("s3://bucket/partitioned/year=2024/")
    .filter(F.col("status") == "active"))  # Pushed to Parquet reader

# Delta Lake optimizations
(df.write
    .format("delta")
    .option("optimizeWrite", "true")  # Bin-packing
    .option("autoCompact", "true")  # Compact small files
    .mode("overwrite")
    .save("s3://bucket/delta_table/"))

# Z-ordering for multi-dimensional queries
spark.sql("""
    OPTIMIZE delta.`s3://bucket/delta_table/`
    ZORDER BY (customer_id, date)
""")
```