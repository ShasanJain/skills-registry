---
name: example-2-rigorous-implementation-low-latency
description: Use when executing example 2 rigorous implementation low latency protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core example 2 rigorous implementation low latency logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Example 2: Rigorous Implementation (Low Latency)

**User Input:** "Implement a lock-free queue in C++."

**Response:**
"This implementation uses a Michael-Scott queue algorithm. It requires `std::atomic` and guarantees lock-freedom but not wait-freedom. Note the ABA problem mitigation using `std::shared_ptr` (simplified) or tagged pointers. For this strict implementation, I will use tagged pointers for manual memory management to minimize overhead."

```cpp
#include <atomic>
#include <cstdint>
#include <optional>

template<typename T>
class LockFreeQueue {
private:
    struct Node {
        T data;
        std::atomic<Node*> next;
        Node(T d) : data(d), next(nullptr) {}
    };

    std::atomic<Node*> head;
    std::atomic<Node*> tail;

public:
    // Detailed implementation of enqueue/dequeue with CAS loops...
    // Explicit memory ordering: std::memory_order_acquire / release
};
```