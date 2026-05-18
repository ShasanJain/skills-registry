# Code Quality Verification: ESLint, TypeScript, and Automated Testing

Code Quality is the absolute operational standard for all feature development. By implementing a strict continuous audit, the engine guarantees that no code is delivered with TS type discrepancies, formatting violations, syntax errors, or broken regression suites. The agent must systematically execute this quality verification routine before finalizing any pull request or marking any implementation milestone as complete.

## ⚙️ Quality Audit SOP

Follow this step-by-step procedure to perform a complete code quality audit:

- **Step 1: Execute Static Type Check**: Run the TypeScript compiler in dry-run mode (e.g., `npx tsc --noEmit` or matching framework commands) to verify all types, interfaces, imports, and exports resolve without a single error.
- **Step 2: Run Linter Diagnostics**: Run ESLint or the local workspace formatter (e.g., `npm run lint` or `npx eslint . --fix`) to automatically detect and correct style violations, unhandled promises, and syntax bugs.
- **Step 3: Run the Regression Suite**: Trigger the full test suite (e.g., `npm run test`, `jest`, or `vitest`) to ensure all existing integration and unit tests pass with zero failures.
- **Step 4: Analyze Test Coverage**: Verify that any new functional code is accompanied by corresponding unit or integration tests, aiming to maintain baseline test coverage.
- **Step 5: Verify Build Compilation**: Execute the production build command (e.g., `npm run build` or framework equivalent) to guarantee that the application compiles into a stable production package without warnings.
- **Step 6: Log Quality Checklist**: Document the verification outcomes in the session walkthrough, noting any unresolved dependencies or package deprecation warnings before hand-off.