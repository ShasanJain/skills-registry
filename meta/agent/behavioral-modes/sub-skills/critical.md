# Critical Defect Protocol: Security Vulnerabilities and Architectural Crashes

Critical Defects are structural failures or high-severity security vulnerabilities that compromise system runtime stability, data privacy, or host security. By implementing a strict triage and containment strategy, the engine guarantees that no code containing SQL injections, authorization bypasses, unhandled race conditions, or infinite recursion loops is ever committed to the repository. The agent must systematically run this critical defect assessment before final delivery.

## ⚙️ Defect Containment SOP

Follow this step-by-step procedure to isolate, patch, and verify critical defects:

- **Step 1: Isolate Security Vulnerabilities**: Perform static analysis to detect code injection vectors (such as SQL injections, Cross-Site Scripting [XSS], or OS command injections) and unauthenticated API endpoints.
- **Step 2: Detect Memory Leaks and Thread Locks**: Inspect complex concurrency loops, listener attachments, and large array allocations to ensure no background threads block the CPU or exhaust system memory.
- **Step 3: Analyze Data Privacy and Leakage**: Verify that no production API keys, environment credentials, OAuth secrets, or personally identifiable information (PII) are logged to stdout or committed to Git.
- **Step 4: Audit Breaking Database Schema Changes**: Assess migrations and schema edits to prevent destructive changes (like dropping columns or changing key constraints) that cause runtime backend queries to crash.
- **Step 5: Apply Immediate Rollback and Mitigation**: If any critical defect is identified, immediately halt deployment, isolate the broken branch, and apply hotfixes or revert to the last stable state.
- **Step 6: Document Retrospective and Hardening Steps**: Create a detailed incident retrospective log, outline why the failure occurred, and implement automated regression test guardrails to prevent future occurrences.