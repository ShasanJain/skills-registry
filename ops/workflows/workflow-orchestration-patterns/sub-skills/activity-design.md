---
name: activity-design
description: Use when executing activity design protocols within the ops sector.
---

# Activity Design: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Activity Design. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Activity Design

1. **Idempotent operations** - Safe to retry
2. **Short-lived** - Seconds to minutes, not hours
3. **Timeout configuration** - Always set timeouts
4. **Heartbeat for long tasks** - Report progress
5. **Error handling** - Distinguish retryable vs non-retryable