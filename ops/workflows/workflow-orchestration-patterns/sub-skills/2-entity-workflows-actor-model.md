---
name: 2-entity-workflows-actor-model
description: Use when executing 2 entity workflows actor model protocols within the ops sector.
---

# 2 Entity Workflows Actor Model: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 2 Entity Workflows Actor Model. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 2. Entity Workflows (Actor Model)

**Purpose**: Long-lived workflow representing single entity instance

**Pattern** (Source: docs.temporal.io/evaluate/use-cases-design-patterns):

- One workflow execution = one entity (cart, account, inventory item)
- Workflow persists for entity lifetime
- Receives signals for state changes
- Supports queries for current state

**Example Use Cases:**

- Shopping cart (add items, checkout, expiration)
- Bank account (deposits, withdrawals, balance checks)
- Product inventory (stock updates, reservations)

**Benefits:**

- Encapsulates entity behavior
- Guarantees consistency per entity
- Natural event sourcing