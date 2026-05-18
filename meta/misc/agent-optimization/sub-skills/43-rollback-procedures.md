---
name: 43-rollback-procedures
description: Use when applying 43 rollback procedures patterns to optimize agent workflows.
---

# 43 Rollback Procedures: Standard Operating Procedure

## ⚙️ Overview
This protocol defines the strict standard for implementing 43 Rollback Procedures. By following this SOP, the engine ensures token efficiency, maximum architectural stability, robust caching, and adherence to all operational guardrails established by the system architecture.

# 4.3 Rollback Procedures

Quick recovery mechanism:

```
Rollback Triggers:
- Success rate drops >10% from baseline
- Critical errors increase >5%
- User complaints spike
- Cost per task increases >20%
- Safety violations detected

Rollback Process:
1. Detect issue via monitoring
2. Alert team immediately
3. Switch to previous stable version
4. Analyze root cause
5. Fix and re-test before retry
```