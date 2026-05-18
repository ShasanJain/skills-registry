## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core skill logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the design sector.

---

## 📚 Reference Material

---
name: templates
description: Project scaffolding templates for new applications. Use when creating new projects from scratch. Contains 12 templates for various tech stacks.
allowed-tools: Read, Glob, Grep
---

# Project Templates

> Quick-start templates for scaffolding new projects.

---

## 🎯 Selective Reading Rule

**Read ONLY the template matching user's project type!**

| Template | Tech Stack | When to Use |
|----------|------------|-------------|
| [nextjs-fullstack](nextjs-fullstack/TEMPLATE.md) | Next.js + Prisma | Full-stack web app |
| [nextjs-saas](nextjs-saas/TEMPLATE.md) | Next.js + Stripe | SaaS product |
| [nextjs-static](nextjs-static/TEMPLATE.md) | Next.js + Framer | Landing page |
| [express-api](express-api/TEMPLATE.md) | Express + JWT | REST API |
| [python-fastapi](python-fastapi/TEMPLATE.md) | FastAPI | Python API |
| [react-native-app](react-native-app/TEMPLATE.md) | Expo + Zustand | Mobile app |
| [flutter-app](flutter-app/TEMPLATE.md) | Flutter + Riverpod | Cross-platform |
| [electron-desktop](electron-desktop/TEMPLATE.md) | Electron + React | Desktop app |
| [chrome-extension](chrome-extension/TEMPLATE.md) | Chrome MV3 | Browser extension |
| [cli-tool](cli-tool/TEMPLATE.md) | Node.js + Commander | CLI app |
| [monorepo-turborepo](monorepo-turborepo/TEMPLATE.md) | Turborepo + pnpm | Monorepo |
| [astro-static](astro-static/TEMPLATE.md) | Astro + MDX | Blog / Docs |

---

## Usage

1. User says "create [type] app"
2. Match to appropriate template
3. Read ONLY that template's TEMPLATE.md
4. Follow its tech stack and structure
