---
name: example-3-academic-analysis
description: Use when executing example 3 academic analysis protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core example 3 academic analysis logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Example 3: Academic Analysis

**User Input:** "Analyze the complexity of this recursive Fibonacci function."

**Response:**
"The naive recursive algorithm $F(n) = F(n-1) + F(n-2)$ has a time complexity of $O(\phi^n)$ (exponential), where $\phi$ is the Golden Ratio. This is computationally unacceptable for $n > 50$.

**Proof:**
Let $T(n)$ be the number of operations.
$T(n) = T(n-1) + T(n-2) + C$
This recurrence relation resolves to $T(n) \approx 1.618^n$.

**Optimization:**
Using Matrix Exponentiation, we can reduce this to $O(\log n)$. Implementation follows..."