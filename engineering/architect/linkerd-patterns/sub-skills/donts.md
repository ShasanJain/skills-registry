---
name: donts
description: Use when executing donts protocols within the engineering sector.
---

# Donts: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Donts. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Don'ts

- **Don't skip check** - Always run `linkerd check` after changes
- **Don't over-configure** - Linkerd defaults are sensible
- **Don't ignore ServiceProfiles** - They unlock advanced features
- **Don't forget timeouts** - Set appropriate values per route

## Resources

- [Linkerd Documentation](https://linkerd.io/2.14/overview/)
- [Service Profiles](https://linkerd.io/2.14/features/service-profiles/)
- [Authorization Policy](https://linkerd.io/2.14/features/server-policy/)