---
name: security
description: Use when executing security protocols within the engineering sector.
---

# Security: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Security. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Security

- Store API credentials in environment variables
- Always verify webhook HMAC signatures before processing
- Validate OAuth state parameter to prevent CSRF
- Request minimal access scopes
- Use session tokens for embedded apps