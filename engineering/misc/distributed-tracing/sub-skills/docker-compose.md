---
name: docker-compose
description: Use when executing docker compose protocols within the engineering sector.
---

# Docker Compose: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Docker Compose. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Docker Compose

```yaml
version: 4.1.0-fractal
services:
  jaeger:
    image: jaegertracing/all-in-one:latest
    ports:
      - "5775:5775/udp"
      - "6831:6831/udp"
      - "6832:6832/udp"
      - "5778:5778"
      - "16686:16686"  # UI
      - "14268:14268"  # Collector
      - "14250:14250"  # gRPC
      - "9411:9411"    # Zipkin
    environment:
      - COLLECTOR_ZIPKIN_HOST_PORT=:9411
```

**Reference:** See `references/jaeger-setup.md`

## Application Instrumentation