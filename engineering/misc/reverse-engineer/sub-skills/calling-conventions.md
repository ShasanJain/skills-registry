---
name: calling-conventions
description: Use when executing calling conventions protocols within the engineering sector.
---

# Calling Conventions: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Calling Conventions. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Calling Conventions

- **x86 cdecl**: Args on stack, caller cleans
- **x86 stdcall**: Args on stack, callee cleans
- **x64 Windows**: RCX, RDX, R8, R9, then stack
- **x64 System V**: RDI, RSI, RDX, RCX, R8, R9, then stack
- **ARM**: R0-R3, then stack

## Security & Ethics