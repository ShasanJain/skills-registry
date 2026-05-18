---
name: resilience-fault-tolerance
description: Use when executing resilience fault tolerance protocols within the engineering sector.
---

# Resilience Fault Tolerance: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Resilience Fault Tolerance. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Resilience & Fault Tolerance

- **Circuit breaker**: Hystrix, resilience4j, failure detection, state management
- **Retry patterns**: Exponential backoff, jitter, retry budgets, idempotency
- **Timeout management**: Request timeouts, connection timeouts, deadline propagation
- **Bulkhead pattern**: Resource isolation, thread pools, connection pools
- **Graceful degradation**: Fallback responses, cached responses, feature toggles
- **Health checks**: Liveness, readiness, startup probes, deep health checks
- **Chaos engineering**: Fault injection, failure testing, resilience validation
- **Backpressure**: Flow control, queue management, load shedding
- **Idempotency**: Idempotent operations, duplicate detection, request IDs
- **Compensation**: Compensating transactions, rollback strategies, saga patterns