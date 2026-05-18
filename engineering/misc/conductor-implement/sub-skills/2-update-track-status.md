---
name: 2-update-track-status
description: Use when executing 2 update track status protocols within the engineering sector.
---

# 2 Update Track Status: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing 2 Update Track Status. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# 2. Update Track Status

In `conductor/tracks.md`:

- Change `[~]` to `[x]` for this track
- Update the "Updated" column

In `conductor/tracks/{trackId}/metadata.json`:

- Set `status: "complete"`
- Set `phases.completed` to total
- Set `tasks.completed` to total
- Update `updated` timestamp

In `conductor/tracks/{trackId}/plan.md`:

- Update header status to `[x] Complete`