---
name: migration-expertise
description: Use when executing migration expertise protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core migration expertise logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Migration Expertise

**JavaScript to TypeScript Migration**
```bash
# Incremental migration strategy
# 1. Enable allowJs and checkJs (merge into existing tsconfig.json):
# Add to existing tsconfig.json:
# {
#   "compilerOptions": {
#     "allowJs": true,
#     "checkJs": true
#   }
# }

# 2. Rename files gradually (.js → .ts)
# 3. Add types file by file using AI assistance
# 4. Enable strict mode features one by one

# Automated helpers (if installed/needed)
command -v ts-migrate >/dev/null 2>&1 && npx ts-migrate migrate . --sources 'src/**/*.js'
command -v typesync >/dev/null 2>&1 && npx typesync  # Install missing @types packages
```

**Tool Migration Decisions**

| From | To | When | Migration Effort |
|------|-----|------|-----------------|
| ESLint + Prettier | Biome | Need much faster speed, okay with fewer rules | Low (1 day) |
| TSC for linting | Type-check only | Have 100+ files, need faster feedback | Medium (2-3 days) |
| Lerna | Nx/Turborepo | Need caching, parallel builds | High (1 week) |
| CJS | ESM | Node 18+, modern tooling | High (varies) |