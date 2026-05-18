---
name: biome-vs-eslint
description: Use when executing biome vs eslint protocols within the engineering sector.
---

# Biome Vs Eslint: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Biome Vs Eslint. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Biome vs ESLint

**Use Biome when:**
- Speed is critical (often faster than traditional setups)
- Want single tool for lint + format
- TypeScript-first project
- Okay with 64 TS rules vs 100+ in typescript-eslint

**Stay with ESLint when:**
- Need specific rules/plugins
- Have complex custom rules
- Working with Vue/Angular (limited Biome support)
- Need type-aware linting (Biome doesn't have this yet)