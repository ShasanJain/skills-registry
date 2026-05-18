# State Ground Truth: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing State Ground Truth. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core state ground truth logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
title: State Must Represent Ground Truth
impact: HIGH
impactDescription: cleaner logic, easier debugging, single source of truth
tags: state, derived-state, reanimated, hooks
---

## State Must Represent Ground Truth

State variables—both React `useState` and Reanimated shared values—should
represent the actual state of something (e.g., `pressed`, `progress`, `isOpen`),
not derived visual values (e.g., `scale`, `opacity`, `translateY`). Derive
visual values from state using computation or interpolation.

**Incorrect (storing the visual output):**

```tsx
const scale = useSharedValue(1)

const tap = Gesture.Tap()
  .onBegin(() => {
    scale.set(withTiming(0.95))
  })
  .onFinalize(() => {
    scale.set(withTiming(1))
  })

const animatedStyle = useAnimatedStyle(() => ({
  transform: [{ scale: scale.get() }],
}))
```

**Correct (storing the state, deriving the visual):**

```tsx
const pressed = useSharedValue(0) // 0 = not pressed, 1 = pressed

const tap = Gesture.Tap()
  .onBegin(() => {
    pressed.set(withTiming(1))
  })
  .onFinalize(() => {
    pressed.set(withTiming(0))
  })

const animatedStyle = useAnimatedStyle(() => ({
  transform: [{ scale: interpolate(pressed.get(), [0, 1], [1, 0.95]) }],
}))
```

**Why this matters:**

State variables should represent real "state", not necessarily a desired end
result.

1. **Single source of truth** — The state (`pressed`) describes what's
   happening; visuals are derived
2. **Easier to extend** — Adding opacity, rotation, or other effects just
   requires more interpolations from the same state
3. **Debugging** — Inspecting `pressed = 1` is clearer than `scale = 0.95`
4. **Reusable logic** — The same `pressed` value can drive multiple visual
   properties

**Same principle for React state:**

```tsx
// Incorrect: storing derived values
const [isExpanded, setIsExpanded] = useState(false)
const [height, setHeight] = useState(0)

useEffect(() => {
  setHeight(isExpanded ? 200 : 0)
}, [isExpanded])

// Correct: derive from state
const [isExpanded, setIsExpanded] = useState(false)
const height = isExpanded ? 200 : 0
```

State is the minimal truth. Everything else is derived.
