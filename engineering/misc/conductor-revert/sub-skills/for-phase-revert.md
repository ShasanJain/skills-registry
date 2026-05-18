---
name: for-phase-revert
description: Use when executing for phase revert protocols within the engineering sector.
---

# For Phase Revert: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing For Phase Revert. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# For Phase Revert

1. Determine task range for the phase by reading plan.md
2. Search for all task commits in that phase:

   ```bash
   git log --oneline --grep="{trackId}" | grep -E "Task {N}\.[0-9]"
   ```

3. Find phase verification commit if exists
4. Find all plan.md update commits for phase tasks
5. Collect all matching commit SHAs in chronological order