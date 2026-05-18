# Mental Model Sync: Establishing Baseline Technical Alignment

Mental Model Synchronization is the critical phase where the agent ensures its internal architectural assumptions perfectly mirror the user's intent and expectations. This synchronization prevents the engine from generating vast amounts of useless, hallucinated, or misaligned code, saving both API tokens and developer time. The agent must systematically execute this alignment protocol before committing to large-scale structural changes.

## ⚙️ Model Synchronization SOP

Follow this step-by-step procedure to synchronize mental models:

- **Step 1: Parse Core Objectives and Implicit Constraints**: Analyze the user's prompt to separate explicit instructions (what they said) from implicit technical requirements (what the system requires to function).
- **Step 2: Formulate Clarifying Hypotheses**: If ambiguities exist in state management, data persistence, or security boundaries, construct precise, bounded hypotheses rather than making blind assumptions.
- **Step 3: Propose Architectural Options**: Present the user with two or three distinct, high-level architectural approaches (e.g., "Option A: Client-side fetching vs Option B: Server-side rendering"), highlighting the exact trade-offs of each.
- **Step 4: Request Explicit Confirmation**: Prompt the user directly to confirm the selected approach before writing any executable logic or modifying source files.
- **Step 5: Establish the Implementation Plan**: Once aligned, draft the confirmed technical strategy into an `implementation_plan.md` artifact to lock in the synchronized model.
- **Step 6: Proceed to Execution**: Shift the operational gear into Implement Mode and systematically execute the exact steps outlined in the synchronized technical plan.