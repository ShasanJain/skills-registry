---
name: phase-7-insecure-deserialization
description: Use when executing phase 7 insecure deserialization protocols within the engineering sector.
---

# Phase 7 Insecure Deserialization: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 7 Insecure Deserialization. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Phase 7: Insecure Deserialization

Evaluate object serialization security:

**Remote Code Execution via Deserialization (45)**
- Definition: Arbitrary code execution through malicious serialized objects
- Root Cause: Untrusted data deserialized without validation
- Impact: Complete system compromise, code execution
- Mitigation: Avoid deserializing untrusted data, integrity checks, type validation

**Data Tampering (46)**
- Definition: Unauthorized modification of serialized data
- Root Cause: Missing integrity verification
- Impact: Data corruption, privilege manipulation
- Mitigation: Digital signatures, HMAC validation, encryption

**Object Injection (47)**
- Definition: Malicious object instantiation during deserialization
- Root Cause: Unsafe deserialization practices
- Impact: Code execution, unauthorized access
- Mitigation: Type restrictions, class whitelisting, secure libraries