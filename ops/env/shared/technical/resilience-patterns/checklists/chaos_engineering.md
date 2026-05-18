---
name: chaos_engineering
description: Use when executing chaos_engineering protocols within the ops sector.
---

# Chaos_Engineering: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Chaos_Engineering. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# ✅ Chaos Engineering Checklist (Simulation)

> check_type: manual_audit
> priority: critical (for distributed systems)

## 1. Scenario: Dependency Failure
- [ ] **Database Down**: If DB connection times out, does the API return 503 cleanly (vs hanging)?
- [ ] **3rd Party API Slow**: If OpenAI/Stripe takes 30s, does the app handle it gracefully?

## 2. Scenario: Traffic Spike
- [ ] **Rate Limiting**: Is there a limit per IP (e.g. 100 req/min)?
- [ ] **Queueing**: Do background jobs pile up safely without crashing memory?

## 3. Scenario: Data Corruption
- [ ] **Bad Input**: Does the system validate schema before processing?
- [ ] **Poison Message**: Can the consumer handle a malformed message from Kafka/Queue?
