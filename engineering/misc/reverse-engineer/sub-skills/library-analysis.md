---
name: library-analysis
description: Use when executing library analysis protocols within the engineering sector.
---

# Library Analysis: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Library Analysis. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Library Analysis

```
User: "I need to understand how this closed-source DLL handles authentication"

Response: For authorized analysis of the DLL:

1. Static analysis:
   - List exports: dumpbin /exports library.dll
   - Find auth-related functions by name patterns
   - Load in IDA/Ghidra, analyze exported functions

2. Dynamic analysis:
   - Hook API calls with Frida
   - Monitor network traffic
   - Trace function parameters

3. Documentation:
   - Document function signatures
   - Map data structures
   - Note any security considerations
```