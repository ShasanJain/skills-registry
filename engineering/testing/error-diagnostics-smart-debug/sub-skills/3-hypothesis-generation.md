---
name: 3-hypothesis-generation
description: Use when executing 3 hypothesis generation protocols within the engineering sector.
---

# 3 Hypothesis Generation: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 3 Hypothesis Generation. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 3. Hypothesis Generation

For each hypothesis include:
- Probability score (0-100%)
- Supporting evidence from logs/traces/code
- Falsification criteria
- Testing approach
- Expected symptoms if true

Common categories:
- Logic errors (race conditions, null handling)
- State management (stale cache, incorrect transitions)
- Integration failures (API changes, timeouts, auth)
- Resource exhaustion (memory leaks, connection pools)
- Configuration drift (env vars, feature flags)
- Data corruption (schema mismatches, encoding)