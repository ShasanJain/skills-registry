---
name: template-3-quick-postmortem-minor-incidents
description: Use when executing template 3 quick postmortem minor incidents protocols within the engineering sector.
---

# Template 3 Quick Postmortem Minor Incidents: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Template 3 Quick Postmortem Minor Incidents. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Template 3: Quick Postmortem (Minor Incidents)

```markdown
# Quick Postmortem: [Brief Title]

**Date**: 2024-01-15 | **Duration**: 12 min | **Severity**: SEV3

## What Happened
API latency spiked to 5s due to cache miss storm after cache flush.

## Timeline
- 10:00 - Cache flush initiated for config update
- 10:02 - Latency alerts fire
- 10:05 - Identified as cache miss storm
- 10:08 - Enabled cache warming
- 10:12 - Latency normalized

## Root Cause
Full cache flush for minor config update caused thundering herd.

## Fix
- Immediate: Enabled cache warming
- Long-term: Implement partial cache invalidation (ENG-999)

## Lessons
Don't full-flush cache in production; use targeted invalidation.
```

## Facilitation Guide