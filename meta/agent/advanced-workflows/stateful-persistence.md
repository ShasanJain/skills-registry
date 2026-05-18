# Stateful Persistence: Checkpoints and Crash Recovery

Stateful Persistence ensures that long-running autonomous tasks can survive system crashes, context window expirations, and human-in-the-loop (HITL) pauses. By actively writing execution states to disk or databases (e.g., using LangGraph patterns), the engine can instantly resume operations from its exact last known good state without starting over.

## ⚙️ State Checkpointing SOP

Follow this step-by-step procedure to manage workflow persistence:

- **Step 1: Initialize Session Checkpoints**: At the start of a major execution block, verify the existence of a state log file (e.g., `task.md` or a JSON telemetry store) to track progress.
- **Step 2: Log Micro-Milestones**: After completing a discrete action (e.g., generating a component, running an ESLint fix), immediately update the persistence log (check off the `[ ]` to `[x]`).
- **Step 3: Pause for HITL Intersections**: If a destructive action (like dropping a SQL table) is required, checkpoint the state, output the pending command, and pause the thread awaiting explicit user approval.
- **Step 4: Execute Fast Recovery**: If the session crashes or the agent is re-instantiated, the first protocol is to parse the `task.md` checkpoint file. Never repeat steps marked as `[x]`.
- **Step 5: Sanitize Corrupted States**: If the checkpoint data is malformed or desynced from the actual codebase, run a fast verification pass (`npm test`) to realign the state graph before continuing.
- **Step 6: Archive Completed States**: Upon absolute project completion, archive the state logs into a final `walkthrough.md` report and clear the active task buffers.
