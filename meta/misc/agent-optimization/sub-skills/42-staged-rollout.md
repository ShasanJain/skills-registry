---
name: 42-staged-rollout
description: Use when applying 42 staged rollout patterns to optimize agent workflows.
---

# 42 Staged Rollout: Standard Operating Procedure

## ⚙️ Overview
This protocol defines the strict standard for implementing 42 Staged Rollout. By following this SOP, the engine ensures token efficiency, maximum architectural stability, robust caching, and adherence to all operational guardrails established by the system architecture.

# 4.2 Staged Rollout

Progressive deployment strategy:

1. **Alpha testing**: Internal team validation (5% traffic)
2. **Beta testing**: Selected users (20% traffic)
3. **Canary release**: Gradual increase (20% → 50% → 100%)
4. **Full deployment**: After success criteria met
5. **Monitoring period**: 7-day observation window