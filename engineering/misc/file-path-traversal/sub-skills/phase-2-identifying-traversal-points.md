---
name: phase-2-identifying-traversal-points
description: Use when executing phase 2 identifying traversal points protocols within the engineering sector.
---

# Phase 2 Identifying Traversal Points: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 2 Identifying Traversal Points. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Phase 2: Identifying Traversal Points

Map application for potential file operations:

```bash
# Parameters that often handle files
?file=
?path=
?page=
?template=
?filename=
?doc=
?document=
?folder=
?dir=
?include=
?src=
?source=
?content=
?view=
?download=
?load=
?read=
?retrieve=
```

Common vulnerable functionality:
- Image loading: `/image?filename=23.jpg`
- Template selection: `?template=blue.php`
- File downloads: `/download?file=report.pdf`
- Document viewers: `/view?doc=manual.pdf`
- Include mechanisms: `?page=about`