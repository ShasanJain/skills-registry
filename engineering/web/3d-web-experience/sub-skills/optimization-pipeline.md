---
name: optimization-pipeline
description: Use when executing optimization pipeline protocols within the engineering sector.
---

# Optimization Pipeline: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Optimization Pipeline. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Optimization Pipeline

```
1. Model in Blender/etc
2. Reduce poly count (< 100K for web)
3. Bake textures (combine materials)
4. Export as GLB
5. Compress with gltf-transform
6. Test file size (< 5MB ideal)
```