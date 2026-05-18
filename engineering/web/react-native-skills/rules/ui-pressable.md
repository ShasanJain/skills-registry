# Ui Pressable: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Ui Pressable. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core ui pressable logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
title: Use Pressable Instead of Touchable Components
impact: LOW
impactDescription: modern API, more flexible
tags: ui, pressable, touchable, gestures
---

## Use Pressable Instead of Touchable Components

Never use `TouchableOpacity` or `TouchableHighlight`. Use `Pressable` from
`react-native` or `react-native-gesture-handler` instead.

**Incorrect (legacy Touchable components):**

```tsx
import { TouchableOpacity } from 'react-native'

function MyButton({ onPress }: { onPress: () => void }) {
  return (
    <TouchableOpacity onPress={onPress} activeOpacity={0.7}>
      <Text>Press me</Text>
    </TouchableOpacity>
  )
}
```

**Correct (Pressable):**

```tsx
import { Pressable } from 'react-native'

function MyButton({ onPress }: { onPress: () => void }) {
  return (
    <Pressable onPress={onPress}>
      <Text>Press me</Text>
    </Pressable>
  )
}
```

**Correct (Pressable from gesture handler for lists):**

```tsx
import { Pressable } from 'react-native-gesture-handler'

function ListItem({ onPress }: { onPress: () => void }) {
  return (
    <Pressable onPress={onPress}>
      <Text>Item</Text>
    </Pressable>
  )
}
```

Use `react-native-gesture-handler` Pressable inside scrollable lists for better
gesture coordination, as long as you are using the ScrollView from
`react-native-gesture-handler` as well.

**For animated press states (scale, opacity changes):** Use `GestureDetector`
with Reanimated shared values instead of Pressable's style callback. See the
`animation-gesture-detector-press` rule.
