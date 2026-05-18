## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core vector_memory_v2_skill logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the intelligence sector.

---

## 📚 Reference Material

---
version: 2.0.0
name: vector-memory-v2
description: "Persistent semantic memory engine for Jack using OpenMemory SDK. Stores facts, events, and procedures across sessions."
---

# 🧠 Vector Memory v2 (Cognitive Memory Engine)

Persistent long-term memory for Jack powered by OpenMemory. Stores and retrieves context using multi-sector semantic search (episodic, semantic, procedural).

## 🛡️ Industrial Protocol
1. **Orchestration**: Jack uses this skill to persist and recall context across sessions.
2. **Execution**: `execution/vector_memory.py` handles all memory operations.
3. **Persistence**: SQLite via OpenMemory (`openmemory.db`), config at `config/memory_config.json`.

## ⌨️ Integrated Commands
| Command | Action |
| :--- | :--- |
| `/remember [text]` | Store a memory (semantic sector). |
| `/remember [text] --sector episodic` | Store as event/session memory. |
| `/recall [query]` | Semantic search across all memories. |
| `/memories` | List all stored memories. |
| `/forget [id]` | Delete a specific memory by ID. |

## 🔄 Auto-Capture
When enabled (`auto_capture: true` in config), Jack auto-stores session summaries at session end using `auto-capture` command. Also triggers when user shares plans via `/remember`.

## 🧪 Verification
```bash
python execution/vector_memory.py store "test memory" --sector semantic
python execution/vector_memory.py recall "test"
python execution/vector_memory.py list
python execution/vector_memory.py forget <id>
```

## 📐 Memory Sectors
| Sector | Purpose | Example |
| :--- | :--- | :--- |
| `semantic` | Facts, preferences, knowledge | "Jack prefers TypeScript" |
| `episodic` | Events, sessions, history | "Session: Fixed UI theme bugs" |
| `procedural` | Patterns, workflows, how-to | "Dashboard uses Next.js + Tailwind v4" |
