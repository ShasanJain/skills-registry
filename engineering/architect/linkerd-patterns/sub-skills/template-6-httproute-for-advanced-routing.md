---
name: template-6-httproute-for-advanced-routing
description: Use when executing template 6 httproute for advanced routing protocols within the engineering sector.
---

# Template 6 Httproute For Advanced Routing: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Template 6 Httproute For Advanced Routing. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Template 6: HTTPRoute for Advanced Routing

```yaml
apiVersion: policy.linkerd.io/v1beta2
kind: HTTPRoute
metadata:
  name: my-route
  namespace: my-namespace
spec:
  parentRefs:
    - name: my-service
      kind: Service
      group: core
      port: 8080
  rules:
    - matches:
        - path:
            type: PathPrefix
            value: /api/v2
        - headers:
            - name: x-api-version
              value: v2
      backendRefs:
        - name: my-service-v2
          port: 8080
    - matches:
        - path:
            type: PathPrefix
            value: /api
      backendRefs:
        - name: my-service-v1
          port: 8080
```