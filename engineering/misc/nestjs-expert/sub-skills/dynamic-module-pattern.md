---
name: dynamic-module-pattern
description: Use when executing dynamic module pattern protocols within the engineering sector.
---

# Dynamic Module Pattern: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Dynamic Module Pattern. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Dynamic Module Pattern

```typescript
@Module({})
export class ConfigModule {
  static forRoot(options: ConfigOptions): DynamicModule {
    return {
      module: ConfigModule,
      providers: [
        {
          provide: 'CONFIG_OPTIONS',
          useValue: options,
        },
      ],
    };
  }
}
```

## Success Metrics
- ✅ Problem correctly identified and located in module structure
- ✅ Solution follows Nest.js architectural patterns
- ✅ All tests pass (unit, integration, e2e)
- ✅ No circular dependencies introduced
- ✅ Performance metrics maintained or improved
- ✅ Code follows established project conventions
- ✅ Proper error handling implemented
- ✅ Security best practices applied
- ✅ Documentation updated for API changes