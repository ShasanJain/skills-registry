---
name: idempotency-requirements
description: Use when executing idempotency requirements protocols within the ops sector.
---

# Idempotency Requirements: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Idempotency Requirements. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Idempotency Requirements

**Why Critical** (Source: docs.temporal.io/activities):

- Activities may execute multiple times
- Network failures trigger retries
- Duplicate execution must be safe

**Implementation Strategies**:

- Idempotency keys (deduplication)
- Check-then-act with unique constraints
- Upsert operations instead of insert
- Track processed request IDs