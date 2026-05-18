---
name: donts
description: Use when executing donts protocols within the ops sector.
---

# Donts: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Donts. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Don'ts

- **Don't disable mTLS** - For convenience in production
- **Don't ignore cert expiry** - Automate rotation
- **Don't use self-signed certs** - Use proper CA hierarchy
- **Don't skip verification** - Verify the full chain

## Resources

- [Istio Security](https://istio.io/latest/docs/concepts/security/)
- [SPIFFE/SPIRE](https://spiffe.io/)
- [cert-manager](https://cert-manager.io/)
- [Zero Trust Architecture (NIST)](https://www.nist.gov/publications/zero-trust-architecture)