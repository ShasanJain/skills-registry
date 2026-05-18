---
name: phase-2-identifying-injection-points
description: Use when executing phase 2 identifying injection points protocols within the security sector.
---

# Phase 2 Identifying Injection Points: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Phase 2 Identifying Injection Points. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Phase 2: Identifying Injection Points

Map application for potential injection surfaces:

```
1. Search bars and search results
2. Comment sections
3. User profile fields
4. Contact forms and feedback
5. Registration forms
6. URL parameters reflected on page
7. Error messages
8. Page titles and headers
9. Hidden form fields
10. Cookie values reflected on page
```

Common vulnerable parameters:
```
?name=
?user=
?search=
?query=
?message=
?title=
?content=
?redirect=
?url=
?page=
```