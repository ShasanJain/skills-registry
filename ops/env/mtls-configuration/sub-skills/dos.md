---
name: dos
description: Use when executing dos protocols within the ops sector.
---

# Dos: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Dos. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Do's

- **Start with PERMISSIVE** - Migrate gradually to STRICT
- **Monitor certificate expiry** - Set up alerts
- **Use short-lived certs** - 24h or less for workloads
- **Rotate CA periodically** - Plan for CA rotation
- **Log TLS errors** - For debugging and audit