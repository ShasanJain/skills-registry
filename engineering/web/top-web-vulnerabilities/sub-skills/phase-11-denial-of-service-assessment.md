---
name: phase-11-denial-of-service-assessment
description: Use when executing phase 11 denial of service assessment protocols within the engineering sector.
---

# Phase 11 Denial Of Service Assessment: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 11 Denial Of Service Assessment. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Phase 11: Denial of Service Assessment

Evaluate availability threats:

**DDoS - Distributed Denial of Service (61)**
- Definition: Overwhelming systems with traffic from multiple sources
- Root Cause: Botnets, amplification attacks
- Impact: Service unavailability, revenue loss
- Mitigation: DDoS protection services, rate limiting, CDN

**Application Layer DoS (62)**
- Definition: Targeting application logic to exhaust resources
- Root Cause: Inefficient code, resource-intensive operations
- Impact: Application unavailability, degraded performance
- Mitigation: Rate limiting, caching, WAF, code optimization

**Resource Exhaustion (63)**
- Definition: Depleting CPU, memory, disk, or network resources
- Root Cause: Inefficient resource management
- Impact: System crashes, service degradation
- Mitigation: Resource quotas, monitoring, load balancing

**Slowloris Attack (64)**
- Definition: Keeping connections open with partial HTTP requests
- Root Cause: No connection timeouts
- Impact: Web server resource exhaustion
- Mitigation: Connection timeouts, request limits, reverse proxy