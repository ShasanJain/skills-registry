---
name: step-4-set-up-environment-variables
description: Use when executing step 4 set up environment variables protocols within the design sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core step 4 set up environment variables logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the design sector.

---

## 📚 Reference Material

# Step 4: Set Up Environment Variables

Create a \`.env\` file:
\`\`\`bash
# Copy example environment file
cp .env.example .env

# Edit with your values
nano .env
\`\`\`

Example \`.env\` content:
\`\`\`
NODE_ENV=development
PORT=3000
DATABASE_URL=postgresql://localhost:5432/mydb
API_KEY=your-api-key-here
\`\`\`