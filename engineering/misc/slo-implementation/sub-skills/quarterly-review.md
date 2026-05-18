---
name: quarterly-review
description: Use when executing quarterly review protocols within the engineering sector.
---

# Quarterly Review: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Quarterly Review. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Quarterly Review

- SLO relevance
- Target adjustments
- Process improvements
- Tooling enhancements

## Best Practices

1. **Start with user-facing services**
2. **Use multiple SLIs** (availability, latency, etc.)
3. **Set achievable SLOs** (don't aim for 100%)
4. **Implement multi-window alerts** to reduce noise
5. **Track error budget** consistently
6. **Review SLOs regularly**
7. **Document SLO decisions**
8. **Align with business goals**
9. **Automate SLO reporting**
10. **Use SLOs for prioritization**

## Reference Files

- `assets/slo-template.md` - SLO definition template
- `references/slo-definitions.md` - SLO definition patterns
- `references/error-budget.md` - Error budget calculations

## Related Skills

- `prometheus-configuration` - For metric collection
- `grafana-dashboards` - For SLO visualization