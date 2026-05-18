---
name: patterns-reference
description: Use when executing patterns reference protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core patterns reference logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Architecture Patterns Reference

> Quick reference for common patterns with usage guidance.

## Data Access Patterns

| Pattern | When to Use | When NOT to Use | Complexity |
|---------|-------------|-----------------|------------|
| **Active Record** | Simple CRUD, rapid prototyping | Complex queries, multiple sources | Low |
| **Repository** | Testing needed, multiple sources | Simple CRUD, single database | Medium |
| **Unit of Work** | Complex transactions | Simple operations | High |
| **Data Mapper** | Complex domain, performance | Simple CRUD, rapid dev | High |

## Domain Logic Patterns

| Pattern | When to Use | When NOT to Use | Complexity |
|---------|-------------|-----------------|------------|
| **Transaction Script** | Simple CRUD, procedural | Complex business rules | Low |
| **Table Module** | Record-based logic | Rich behavior needed | Low |
| **Domain Model** | Complex business logic | Simple CRUD | Medium |
| **DDD (Full)** | Complex domain, domain experts | Simple domain, no experts | High |

## Distributed System Patterns

| Pattern | When to Use | When NOT to Use | Complexity |
|---------|-------------|-----------------|------------|
| **Modular Monolith** | Small teams, unclear boundaries | Clear contexts, different scales | Medium |
| **Microservices** | Different scales, large teams | Small teams, simple domain | Very High |
| **Event-Driven** | Real-time, loose coupling | Simple workflows, strong consistency | High |
| **CQRS** | Read/write performance diverges | Simple CRUD, same model | High |
| **Saga** | Distributed transactions | Single database, simple ACID | High |

## API Patterns

| Pattern | When to Use | When NOT to Use | Complexity |
|---------|-------------|-----------------|------------|
| **REST** | Standard CRUD, resources | Real-time, complex queries | Low |
| **GraphQL** | Flexible queries, multiple clients | Simple CRUD, caching needs | Medium |
| **gRPC** | Internal services, performance | Public APIs, browser clients | Medium |
| **WebSocket** | Real-time updates | Simple request/response | Medium |

---

## Simplicity Principle

**"Start simple, add complexity only when proven necessary."**

- You can always add patterns later
- Removing complexity is MUCH harder than adding it
- When in doubt, choose simpler option
