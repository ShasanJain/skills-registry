---
name: configuration-file
description: Use when executing configuration file protocols within the engineering sector.
---

# Configuration File: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Configuration File. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Configuration File

**Location**: `.claude/skills/skill-rules.json`

Defines:
- All skills and their trigger conditions
- Enforcement levels (block, suggest, warn)
- File path patterns (glob)
- Content detection patterns (regex)
- Skip conditions (session tracking, file markers, env vars)

---

## Skill Types