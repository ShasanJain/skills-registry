---
name: manual-rotation-process
description: Use when executing manual rotation process protocols within the security sector.
---

# Manual Rotation Process: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Manual Rotation Process. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Manual Rotation Process

1. Generate new secret
2. Update secret in secret store
3. Update applications to use new secret
4. Verify functionality
5. Revoke old secret

## External Secrets Operator