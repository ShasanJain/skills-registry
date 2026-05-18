---
name: deterministic-outer-loops
description: Use when executing deterministic outer loops protocols within the engineering sector.
---

# Deterministic Outer Loops: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Deterministic Outer Loops. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Deterministic Outer Loops

**Wrap agent outputs with rule-based validation (NOT LLM-judged):**

```
1. Agent generates output
2. Run linter (deterministic)
3. Run tests (deterministic)
4. Check compilation (deterministic)
5. Only then: human or AI review
```