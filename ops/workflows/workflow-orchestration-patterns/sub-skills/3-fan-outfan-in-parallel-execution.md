---
name: 3-fan-outfan-in-parallel-execution
description: Use when executing 3 fan outfan in parallel execution protocols within the ops sector.
---

# 3 Fan Outfan In Parallel Execution: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 3 Fan Outfan In Parallel Execution. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 3. Fan-Out/Fan-In (Parallel Execution)

**Purpose**: Execute multiple tasks in parallel, aggregate results

**Pattern:**

- Spawn child workflows or parallel activities
- Wait for all to complete
- Aggregate results
- Handle partial failures

**Scaling Rule** (Source: temporal.io/blog/workflow-engine-principles):

- Don't scale individual workflows
- For 1M tasks: spawn 1K child workflows × 1K tasks each
- Keep each workflow bounded