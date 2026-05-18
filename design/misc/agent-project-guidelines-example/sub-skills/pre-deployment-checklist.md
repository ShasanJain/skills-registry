---
name: pre-deployment-checklist
description: Use when executing pre deployment checklist protocols within the design sector.
---

# Pre Deployment Checklist: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Pre Deployment Checklist. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Pre-Deployment Checklist

- [ ] All tests passing locally
- [ ] `npm run build` succeeds (frontend)
- [ ] `poetry run pytest` passes (backend)
- [ ] No hardcoded secrets
- [ ] Environment variables documented
- [ ] Database migrations ready