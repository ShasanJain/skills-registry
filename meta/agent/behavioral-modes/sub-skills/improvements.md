# Continuous Refactoring Protocol: Code Optimization and Debt Reduction

Continuous Refactoring is the operational process of cleaning up code structure, improving performance, and systematically removing technical debt without altering external system behaviors. By establishing a dedicated refactoring loop, the engine ensures that codebases remain maintainable, scalable, and easy to extend over time. The agent must systematically run this optimization cycle during implement and review phases.

## ⚙️ Refactoring SOP

Follow this step-by-step procedure to execute structural code improvements:

- **Step 1: Identify and Remove Duplicate Logic**: Scan files for copy-pasted or redundant functions, extracting them into modular, reusable helper classes or utility modules.
- **Step 2: Optimize Algorithmic Time Complexity**: Analyze database queries, data sorting routines, and mapping iterations to replace nested loops (`O(N^2)`) with clean indexing or key-value lookups (`O(1)` or `O(N)`).
- **Step 3: Simplify Complex Conditional Branching**: Flatten deeply nested `if-else` blocks using early returns, guard clauses, polymorphism, or simple dictionary mappings.
- **Step 4: Decouple Magic Constants with Typed Interfaces**: Replace raw strings or numbers hardcoded in logic with clear, descriptive configuration values, global constants, or TypeScript Enums.
- **Step 5: Enhance Naming Conventions and Type Clarity**: Rename vague variables (e.g., `data`, `res`, `x`) with descriptive business domain terms and enrich types with exact interfaces or schemas.
- **Step 6: Document Architectural Walkthrough and Performance Gains**: Highlight refactored modules in the final walkthrough, quantifying memory savings or runtime execution speedups.