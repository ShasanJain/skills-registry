---
name: activities-external-interactions
description: Use when executing activities external interactions protocols within the ops sector.
---

# Activities External Interactions: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Activities External Interactions. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Activities (External Interactions)

**Characteristics:**

- Handle all external system interactions
- Can be non-deterministic (API calls, DB writes)
- Include built-in timeouts and retry logic
- **Must be idempotent** (calling N times = calling once)
- Short-lived (seconds to minutes typically)

**Example activity tasks:**

- Call payment gateway API
- Write to database
- Send emails or notifications
- Query external services