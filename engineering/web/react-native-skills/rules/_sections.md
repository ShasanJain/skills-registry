---
name: _sections
description: Use when executing _sections protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core _sections logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Sections

This file defines all sections, their ordering, impact levels, and descriptions.
The section ID (in parentheses) is the filename prefix used to group rules.

---

## 1. Core Rendering (rendering)

**Impact:** CRITICAL  
**Description:** Fundamental React Native rendering rules. Violations cause
runtime crashes or broken UI.

## 2. List Performance (list-performance)

**Impact:** HIGH  
**Description:** Optimizing virtualized lists (FlatList, LegendList, FlashList)
for smooth scrolling and fast updates.

## 3. Animation (animation)

**Impact:** HIGH  
**Description:** GPU-accelerated animations, Reanimated patterns, and avoiding
render thrashing during gestures.

## 4. Scroll Performance (scroll)

**Impact:** HIGH  
**Description:** Tracking scroll position without causing render thrashing.

## 5. Navigation (navigation)

**Impact:** HIGH  
**Description:** Using native navigators for stack and tab navigation instead of
JS-based alternatives.

## 6. React State (react-state)

**Impact:** MEDIUM  
**Description:** Patterns for managing React state to avoid stale closures and
unnecessary re-renders.

## 7. State Architecture (state)

**Impact:** MEDIUM  
**Description:** Ground truth principles for state variables and derived values.

## 8. React Compiler (react-compiler)

**Impact:** MEDIUM  
**Description:** Compatibility patterns for React Compiler with React Native and
Reanimated.

## 9. User Interface (ui)

**Impact:** MEDIUM  
**Description:** Native UI patterns for images, menus, modals, styling, and
platform-consistent interfaces.

## 10. Design System (design-system)

**Impact:** MEDIUM  
**Description:** Architecture patterns for building maintainable component
libraries.

## 11. Monorepo (monorepo)

**Impact:** LOW  
**Description:** Dependency management and native module configuration in
monorepos.

## 12. Third-Party Dependencies (imports)

**Impact:** LOW  
**Description:** Wrapping and re-exporting third-party dependencies for
maintainability.

## 13. JavaScript (js)

**Impact:** LOW  
**Description:** Micro-optimizations like hoisting expensive object creation.

## 14. Fonts (fonts)

**Impact:** LOW  
**Description:** Native font loading for improved performance.
