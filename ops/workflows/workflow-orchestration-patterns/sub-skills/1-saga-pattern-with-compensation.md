---
name: 1-saga-pattern-with-compensation
description: Use when executing 1 saga pattern with compensation protocols within the ops sector.
---

# 1 Saga Pattern With Compensation: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 1 Saga Pattern With Compensation. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 1. Saga Pattern with Compensation

**Purpose**: Implement distributed transactions with rollback capability

**Pattern** (Source: temporal.io/blog/compensating-actions-part-of-a-complete-breakfast-with-sagas):

```
For each step:
  1. Register compensation BEFORE executing
  2. Execute the step (via activity)
  3. On failure, run all compensations in reverse order (LIFO)
```

**Example: Payment Workflow**

1. Reserve inventory (compensation: release inventory)
2. Charge payment (compensation: refund payment)
3. Fulfill order (compensation: cancel fulfillment)

**Critical Requirements:**

- Compensations must be idempotent
- Register compensation BEFORE executing step
- Run compensations in reverse order
- Handle partial failures gracefully