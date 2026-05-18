---
name: if-argument-provided
description: Use when executing if argument provided protocols within the engineering sector.
---

# If Argument Provided: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing If Argument Provided. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# If argument provided:

Parse the argument format:

**Full track:** `{trackId}`

- Example: `auth_20250115`
- Reverts all commits for the entire track

**Specific phase:** `{trackId}:phase{N}`

- Example: `auth_20250115:phase2`
- Reverts commits for phase N and all subsequent phases

**Specific task:** `{trackId}:task{X.Y}`

- Example: `auth_20250115:task2.3`
- Reverts commits for task X.Y only