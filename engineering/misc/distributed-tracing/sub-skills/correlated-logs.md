---
name: correlated-logs
description: Use when executing correlated logs protocols within the engineering sector.
---

# Correlated Logs: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Correlated Logs. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Correlated Logs

```python
import logging
from opentelemetry import trace

logger = logging.getLogger(__name__)

def process_request():
    span = trace.get_current_span()
    trace_id = span.get_span_context().trace_id

    logger.info(
        "Processing request",
        extra={"trace_id": format(trace_id, '032x')}
    )
```

## Troubleshooting

**No traces appearing:**
- Check collector endpoint
- Verify network connectivity
- Check sampling configuration
- Review application logs

**High latency overhead:**
- Reduce sampling rate
- Use batch span processor
- Check exporter configuration

## Reference Files

- `references/jaeger-setup.md` - Jaeger installation
- `references/instrumentation.md` - Instrumentation patterns
- `assets/jaeger-config.yaml.template` - Jaeger configuration

## Related Skills

- `prometheus-configuration` - For metrics
- `grafana-dashboards` - For visualization
- `slo-implementation` - For latency SLOs