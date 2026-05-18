# Standard Coding Practices: Modular Design Patterns and Error Resiliency

Standard Coding Practices are the foundational guardrails that ensure code remains clean, secure, and robust against unexpected runtime environments. By establishing a dedicated clean-code design strategy, the engine guarantees that all engineered modules maintain clear interfaces, robust exception boundaries, and testable logic. The agent must systematically incorporate these positive patterns into all structural development.

## ⚙️ Standard Architecture SOP

Follow this step-by-step procedure to implement standard, high-quality code structures:

- **Step 1: Enforce Modular Domain Decoupling**: Separate business logic, API route endpoints, and data access layers into isolated modules to avoid tight coupling and circular dependencies.
- **Step 2: Implement Secure Input Validation**: Enforce strict sanitization and schema validations (e.g., using Zod, Pydantic, or matching libraries) for all incoming user parameters and API payloads.
- **Step 3: Establish Robust Exception Boundaries**: Wrap execution pathways in precise try-catch blocks, ensuring failures are gracefully handled, errors are fully logged, and system state is safely recovered.
- **Step 4: Design Standardized API Signatures**: Build clean, predictable API pathways returning consistent HTTP status codes, structured JSON payloads, and clear, human-readable error messages.
- **Step 5: Write Modular Unit and Integration Tests**: Ensure any logical routine has dedicated mock unit tests verifying baseline conditions, extreme edge inputs, and potential failure cases.
- **Step 6: Document Architectural Layouts Clearly**: Maintain up-to-date documentation explaining data flow, design decisions, and system requirements directly in the module's header or markdown files.