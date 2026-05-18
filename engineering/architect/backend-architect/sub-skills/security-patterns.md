---
name: security-patterns
description: Use when executing security patterns protocols within the engineering sector.
---

# Security Patterns: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Security Patterns. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Security Patterns

- **Input validation**: Schema validation, sanitization, allowlisting
- **Rate limiting**: Token bucket, leaky bucket, sliding window, distributed rate limiting
- **CORS**: Cross-origin policies, preflight requests, credential handling
- **CSRF protection**: Token-based, SameSite cookies, double-submit patterns
- **SQL injection prevention**: Parameterized queries, ORM usage, input validation
- **API security**: API keys, OAuth scopes, request signing, encryption
- **Secrets management**: Vault, AWS Secrets Manager, environment variables
- **Content Security Policy**: Headers, XSS prevention, frame protection
- **API throttling**: Quota management, burst limits, backpressure
- **DDoS protection**: CloudFlare, AWS Shield, rate limiting, IP blocking