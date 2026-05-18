---
name: pci-compliance-essentials
description: Use when executing pci compliance essentials protocols within the engineering sector.
---

# Pci Compliance Essentials: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Pci Compliance Essentials. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# PCI Compliance Essentials

- **Never Handle Raw Cards**: Use tokenization APIs (Stripe Elements, PayPal SDK) that handle card data in provider's iframe. NEVER store, process, or transmit raw card numbers.
- **Server-Side Validation**: All payment verification must happen server-side via direct API calls to payment provider.
- **Environment Separation**: Test credentials must fail in production. Misconfigured gateways commonly accept test cards on live sites.

## Common Failures

**Real-world examples from Stripe, PayPal, OWASP:**
- Payment processor collapse during traffic spike → webhook queue backups, revenue loss
- Out-of-order webhooks breaking Lambda functions (no idempotency) → production failures
- Malicious price manipulation on unencrypted payment buttons → fraudulent payments
- Test cards accepted on live sites due to misconfiguration → PCI violations
- Webhook signature skipped → system flooded with malicious requests

**Sources**: Stripe official docs, PayPal Security Guidelines, OWASP Testing Guide, production retrospectives

## Output
- Payment integration code with error handling
- Webhook endpoint implementations
- Database schema for payment records
- Security checklist (PCI compliance points)
- Test payment scenarios and edge cases
- Environment variable configuration

Always use official SDKs. Include both server-side and client-side code where needed.