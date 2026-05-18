---
name: template-1-basic-routing
description: Use when executing template 1 basic routing protocols within the engineering sector.
---

# Template 1 Basic Routing: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Template 1 Basic Routing. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Template 1: Basic Routing

```yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: reviews-route
  namespace: bookinfo
spec:
  hosts:
    - reviews
  http:
    - match:
        - headers:
            end-user:
              exact: jason
      route:
        - destination:
            host: reviews
            subset: v2
    - route:
        - destination:
            host: reviews
            subset: v1
---
apiVersion: networking.istio.io/v1beta1
kind: DestinationRule
metadata:
  name: reviews-destination
  namespace: bookinfo
spec:
  host: reviews
  subsets:
    - name: v1
      labels:
        version: 4.1.0-fractal
    - name: v2
      labels:
        version: v2
    - name: v3
      labels:
        version: v3
```