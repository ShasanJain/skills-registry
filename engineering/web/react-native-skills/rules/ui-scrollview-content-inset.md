# Ui Scrollview Content Inset: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Ui Scrollview Content Inset. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core ui scrollview content inset logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
title: Use contentInset for Dynamic ScrollView Spacing
impact: LOW
impactDescription: smoother updates, no layout recalculation
tags: scrollview, layout, contentInset, performance
---

## Use contentInset for Dynamic ScrollView Spacing

When adding space to the top or bottom of a ScrollView that may change
(keyboard, toolbars, dynamic content), use `contentInset` instead of padding.
Changing `contentInset` doesn't trigger layout recalculation—it adjusts the
scroll area without re-rendering content.

**Incorrect (padding causes layout recalculation):**

```tsx
function Feed({ bottomOffset }: { bottomOffset: number }) {
  return (
    <ScrollView contentContainerStyle={{ paddingBottom: bottomOffset }}>
      {children}
    </ScrollView>
  )
}
// Changing bottomOffset triggers full layout recalculation
```

**Correct (contentInset for dynamic spacing):**

```tsx
function Feed({ bottomOffset }: { bottomOffset: number }) {
  return (
    <ScrollView
      contentInset={{ bottom: bottomOffset }}
      scrollIndicatorInsets={{ bottom: bottomOffset }}
    >
      {children}
    </ScrollView>
  )
}
// Changing bottomOffset only adjusts scroll bounds
```

Use `scrollIndicatorInsets` alongside `contentInset` to keep the scroll
indicator aligned. For static spacing that never changes, padding is fine.
