## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core measuring dom nodes logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the design sector.

---

## 📚 Reference Material

---
name: measuring-dom-nodes
description: Measuring DOM element dimensions in Remotion
metadata:
  tags: measure, layout, dimensions, getBoundingClientRect, scale
---

# Measuring DOM nodes in Remotion

Remotion applies a `scale()` transform to the video container, which affects values from `getBoundingClientRect()`. Use `useCurrentScale()` to get correct measurements.

## Measuring element dimensions

```tsx
import { useCurrentScale } from "remotion";
import { useRef, useEffect, useState } from "react";

export const MyComponent = () => {
  const ref = useRef<HTMLDivElement>(null);
  const scale = useCurrentScale();
  const [dimensions, setDimensions] = useState({ width: 0, height: 0 });

  useEffect(() => {
    if (!ref.current) return;
    const rect = ref.current.getBoundingClientRect();
    setDimensions({
      width: rect.width / scale,
      height: rect.height / scale,
    });
  }, [scale]);

  return <div ref={ref}>Content to measure</div>;
};
```

