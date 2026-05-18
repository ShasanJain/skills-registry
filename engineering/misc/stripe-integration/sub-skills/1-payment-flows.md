---
name: 1-payment-flows
description: Use when executing 1 payment flows protocols within the engineering sector.
---

# 1 Payment Flows: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 1 Payment Flows. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 1. Payment Flows

**Checkout Session (Hosted)**
- Stripe-hosted payment page
- Minimal PCI compliance burden
- Fastest implementation
- Supports one-time and recurring payments

**Payment Intents (Custom UI)**
- Full control over payment UI
- Requires Stripe.js for PCI compliance
- More complex implementation
- Better customization options

**Setup Intents (Save Payment Methods)**
- Collect payment method without charging
- Used for subscriptions and future payments
- Requires customer confirmation