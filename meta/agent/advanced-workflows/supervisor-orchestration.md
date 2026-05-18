# Supervisor Orchestration: Multi-Agent Task Routing

Supervisor Orchestration is the modern architectural pattern for handling complex, multi-phase projects. Instead of a single agent attempting to write a database, backend, and frontend concurrently, the engine acts as a Supervisor. It decomposes the massive objective into isolated sub-tasks and delegates them sequentially to highly specialized operational modes (workers).

## ⚙️ Task Orchestration SOP

Follow this step-by-step procedure to execute Supervisor-Worker routing:

- **Step 1: Parse the Macro Objective**: Analyze the overarching user request (e.g., "Build a full-stack Next.js app with Redis caching") and identify the distinct domain boundaries.
- **Step 2: Generate the Task Dependency Graph**: Map out the explicit execution order. You cannot build a frontend without the API, and you cannot build the API without the database schema.
- **Step 3: Dispatch Worker Modes**: Shift into specialized implementation gears. First, enter Database Mode to scaffold SQLite/Prisma schemas. Next, shift to Backend Mode for the API. Finally, shift to Frontend Mode for React components.
- **Step 4: Enforce Boundary Hand-offs**: Ensure that the output of Worker A perfectly matches the input requirements of Worker B. Validate API payloads against TS interfaces before starting the UI.
- **Step 5: Run Global Integration Tests**: Once all workers complete their domains, compile the entire system and execute `npm run build` or end-to-end integration tests (like Cypress/Playwright).
- **Step 6: Output Unified Walkthrough**: Aggregate the individual worker logs into a single, comprehensive executive summary detailing the fully orchestrated solution.
