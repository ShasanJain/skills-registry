---
name: 4-async-callback-pattern
description: Use when executing 4 async callback pattern protocols within the ops sector.
---

# 4 Async Callback Pattern: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 4 Async Callback Pattern. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 4. Async Callback Pattern

**Purpose**: Wait for external event or human approval

**Pattern:**

- Workflow sends request and waits for signal
- External system processes asynchronously
- Sends signal to resume workflow
- Workflow continues with response

**Use Cases:**

- Human approval workflows
- Webhook callbacks
- Long-running external processes

## State Management and Determinism