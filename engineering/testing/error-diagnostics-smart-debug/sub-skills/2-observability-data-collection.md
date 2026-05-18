---
name: 2-observability-data-collection
description: Use when executing 2 observability data collection protocols within the engineering sector.
---

# 2 Observability Data Collection: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 2 Observability Data Collection. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 2. Observability Data Collection

For production/staging issues, gather:
- Error tracking (Sentry, Rollbar, Bugsnag)
- APM metrics (DataDog, New Relic, Dynatrace)
- Distributed traces (Jaeger, Zipkin, Honeycomb)
- Log aggregation (ELK, Splunk, Loki)
- Session replays (LogRocket, FullStory)

Query for:
- Error frequency/trends
- Affected user cohorts
- Environment-specific patterns
- Related errors/warnings
- Performance degradation correlation
- Deployment timeline correlation