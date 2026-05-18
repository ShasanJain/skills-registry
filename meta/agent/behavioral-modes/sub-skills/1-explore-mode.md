# Explore Mode: Systematic Context Discovery and Mapping

Exploration Mode is the mandatory operational state activated when entering an unfamiliar codebase, handling an ambiguous task, or encountering a new runtime environment. Instead of immediately writing or modifying code, the engine focuses entirely on mapping dependencies, reading documentation, and understanding structural boundaries to prevent accidental regressions and broken systems.

## ⚙️ Exploration & Mapping SOP

Follow this step-by-step procedure to explore and map environments:

- **Step 1: Discover High-Level Architecture**: Run root-level scans (using directory listing or workspace maps) to identify core structural patterns, configuration files, and major module directories.
- **Step 2: Trace Dependency Graphs**: Analyze `package.json`, `requirements.txt`, or equivalent dependency manifests to understand third-party libraries and runtime requirements.
- **Step 3: Map Entry Points and Routes**: Locate system entry points (e.g., `main.py`, `index.ts`, or routing modules) and trace execution flow into the deepest business logic layers.
- **Step 4: Audit Existing Data Schemas**: Inspect database models, API type definitions, and ORM schemas to construct a precise mental model of data structures and relationships.
- **Step 5: Identify Constraints and Gotchas**: Search for `.env.example` files, global configuration limits, and hardcoded legacy constraints to prevent accidental overrides during future implementation phases.
- **Step 6: Output Structural Dossier**: Generate a concise structural summary (or `implementation_plan.md`) outlining the discovered constraints before shifting out of Explore Mode into Implementation.