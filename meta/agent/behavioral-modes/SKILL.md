# Behavioral Modes: Adaptive Agent Operational Profiles

Behavioral Modes define Jack's dynamic operational profiles, adapting cognitive focus, communication formats, and execution protocols based on the target task. By dynamically shifting operational characteristics, the engine optimizes performance, increases code safety, and minimizes token overhead. The agent must select the appropriate behavioral mode at the start of each task or major milestone.

## ⚙️ Mode Transition SOP

Follow this step-by-step procedure to manage and execute behavioral mode transitions:

- **Step 1: Parse and Classify Task Intent**: Analyze the user's initial prompt or command to classify the objective into one of six categories: exploration, architecture design, logic writing, troubleshooting, code quality inspection, or production deployment.
- **Step 2: Transition to Target Mode**: Shift cognitive settings to the designated operational profile (e.g., BRAINSTORM for design, IMPLEMENT for code creation, or DEBUG for fixing stack traces).
- **Step 3: Apply Communication Modifiers**: Adjust response tone and density (e.g., use highly verbose and visual explanations in TEACH mode, but shift to ultra-terse BLUF formatting in SHIP and IMPLEMENT modes).
- **Step 4: Execute Mode-Specific Guardrails**: Apply exact verification gates corresponding to the active mode (e.g., run static code audits using `npm run lint`, verify TypeScript (`TS`) interfaces, and validate API inputs with `Zod` during REVIEW and DEBUG modes).
- **Step 5: Document Sync and State Reversion**: Log the transition in the active session metadata and revert to the baseline master orchestration state once the specific sub-task is successfully resolved.

```bash
# Example Transition Trigger Check
python execution/verify_state.py --mode=SHIP --check=eslint
```

---

## 🧠 Available Operational Profiles

Explore the specialized sub-skills for each operational mode:

### Phase 1: Exploration and Brainstorming
* **[1. 🔭 EXPLORE Mode](./sub-skills/1-explore-mode.md)**: Deep exploration and architectural mapping.
* **[2. 🧠 BRAINSTORM Mode](./sub-skills/1-brainstorm-mode.md)**: Conceptual brainstorming and feature ideation.
* **[3. 🗺️ PLAN-EXECUTE-CRITIC (PEC)](./sub-skills/2-plan-execute-critic-pec.md)**: High-density implementation planning and critique loops.
* **[4. 🧠 MENTAL MODEL SYNC](./sub-skills/3-mental-model-sync.md)**: Establishing baseline alignment between user intent and agent assumptions.

### Phase 2: Implementation and Debugging
* **[5. ⚡ IMPLEMENT Mode](./sub-skills/2-implement-mode.md)**: Pure code generation, scaffolding, and feature engineering.
* **[6. 🔍 DEBUG Mode](./sub-skills/3-debug-mode.md)**: Resolving compiler crashes, logic flaws, and runtime issues.
* **[7. 📚 TEACH Mode](./sub-skills/5-teach-mode.md)**: Conceptual walkthroughs and architectural documentation.

### Phase 3: Review and Deployment
* **[8. 📋 REVIEW Mode](./sub-skills/4-review-mode.md)**: Security audits, optimization reviews, and compliance checks.
  * **[🔴 Critical Review Protocol](./sub-skills/critical.md)**
  * **[🟠 Improvements Checklist](./sub-skills/improvements.md)**
  * **[🟢 Good Patterns Reference](./sub-skills/good.md)**
* **[9. 🚀 SHIP Mode](./sub-skills/6-ship-mode.md)**: Production readiness, build validation, and cloud deployment.
  * **[✅ Code Quality Audit](./sub-skills/code-quality.md)**
  * **[✅ Security Hardening](./sub-skills/security.md)**
  * **[✅ Performance Verification](./sub-skills/performance.md)**
  * **[🚀 Ready to Deploy Checkpoint](./sub-skills/ready-to-deploy.md)**
