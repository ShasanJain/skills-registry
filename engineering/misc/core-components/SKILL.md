# Skill: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Skill. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core skill logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
version: 4.1.0-fractal
name: core-components
description: Core component library and design system patterns. Use when building UI, using design tokens, or working with the component library.
---

# Core Components

## Design System Overview

Use components from your core library instead of raw platform components. This ensures consistent styling and behavior.

## Design Tokens

**NEVER hard-code values. Always use design tokens.**

## 🧠 Knowledge Modules (Fractal Skills)

### 1. [Spacing Tokens](./sub-skills/spacing-tokens.md)
### 2. [Color Tokens](./sub-skills/color-tokens.md)
### 3. [Typography Tokens](./sub-skills/typography-tokens.md)
### 4. [Box](./sub-skills/box.md)
### 5. [HStack / VStack](./sub-skills/hstack-vstack.md)
### 6. [Text](./sub-skills/text.md)
### 7. [Button](./sub-skills/button.md)
### 8. [Input](./sub-skills/input.md)
### 9. [Card](./sub-skills/card.md)
### 10. [Screen Layout](./sub-skills/screen-layout.md)
### 11. [Form Layout](./sub-skills/form-layout.md)
### 12. [List Item Layout](./sub-skills/list-item-layout.md)
