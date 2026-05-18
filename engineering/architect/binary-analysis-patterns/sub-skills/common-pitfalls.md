---
name: common-pitfalls
description: Use when executing common pitfalls protocols within the engineering sector.
---

# Common Pitfalls: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Common Pitfalls. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Common Pitfalls

- **Optimizer artifacts**: Code may not match source structure
- **Inline functions**: Functions may be expanded inline
- **Tail call optimization**: `jmp` instead of `call` + `ret`
- **Dead code**: Unreachable code from optimization
- **Position-independent code**: RIP-relative addressing