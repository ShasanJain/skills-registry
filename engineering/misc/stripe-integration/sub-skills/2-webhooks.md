---
name: 2-webhooks
description: Use when executing 2 webhooks protocols within the engineering sector.
---

# 2 Webhooks: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 2 Webhooks. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 2. Webhooks

**Critical Events:**
- `payment_intent.succeeded`: Payment completed
- `payment_intent.payment_failed`: Payment failed
- `customer.subscription.updated`: Subscription changed
- `customer.subscription.deleted`: Subscription canceled
- `charge.refunded`: Refund processed
- `invoice.payment_succeeded`: Subscription payment successful