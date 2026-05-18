# Animation Derived Value: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Animation Derived Value. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core animation derived value logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
title: Prefer useDerivedValue Over useAnimatedReaction
impact: MEDIUM
impactDescription: cleaner code, automatic dependency tracking
tags: animation, reanimated, derived-value
---

## Prefer useDerivedValue Over useAnimatedReaction

When deriving a shared value from another, use `useDerivedValue` instead of
`useAnimatedReaction`. Derived values are declarative, automatically track
dependencies, and return a value you can use directly. Animated reactions are
for side effects, not derivations.

**Incorrect (useAnimatedReaction for derivation):**

```tsx
import { useSharedValue, useAnimatedReaction } from 'react-native-reanimated'

function MyComponent() {
  const progress = useSharedValue(0)
  const opacity = useSharedValue(1)

  useAnimatedReaction(
    () => progress.value,
    (current) => {
      opacity.value = 1 - current
    }
  )

  // ...
}
```

**Correct (useDerivedValue):**

```tsx
import { useSharedValue, useDerivedValue } from 'react-native-reanimated'

function MyComponent() {
  const progress = useSharedValue(0)

  const opacity = useDerivedValue(() => 1 - progress.get())

  // ...
}
```

Use `useAnimatedReaction` only for side effects that don't produce a value
(e.g., triggering haptics, logging, calling `runOnJS`).

Reference:
[Reanimated useDerivedValue](https://docs.swmansion.com/react-native-reanimated/docs/core/useDerivedValue)
