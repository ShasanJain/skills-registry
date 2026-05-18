---
name: choose-appropriate-slos
description: Use when executing choose appropriate slos protocols within the engineering sector.
---

# Choose Appropriate Slos: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Choose Appropriate Slos. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Choose Appropriate SLOs

**Consider:**
- User expectations
- Business requirements
- Current performance
- Cost of reliability
- Competitor benchmarks

**Example SLOs:**
```yaml
slos:
  - name: api_availability
    target: 99.9
    window: 28d
    sli: |
      sum(rate(http_requests_total{status!~"5.."}[28d]))
      /
      sum(rate(http_requests_total[28d]))

  - name: api_latency_p95
    target: 99
    window: 28d
    sli: |
      sum(rate(http_request_duration_seconds_bucket{le="0.5"}[28d]))
      /
      sum(rate(http_request_duration_seconds_count[28d]))
```

## Error Budget Calculation