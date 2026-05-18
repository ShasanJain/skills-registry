---
name: architectural-coherence
description: Use when executing architectural coherence protocols within the engineering sector.
---

# Architectural Coherence: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Architectural Coherence. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Architectural Coherence

1. **Dependency Direction**: Inner layers don't depend on outer layers
2. **SOLID Principles**:
   - Single Responsibility, Open/Closed, Liskov Substitution
   - Interface Segregation, Dependency Inversion
3. **Anti-patterns**:
   - Singleton (global state), God objects (>500 lines, >20 methods)
   - Anemic models, Shotgun surgery