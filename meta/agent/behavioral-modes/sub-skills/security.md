# Security Hardening: Vulnerability Mitigation and Auditing

Security Hardening is the non-negotiable process of systematically eliminating attack vectors, data exposure risks, and injection flaws from the codebase. The engine is strictly prohibited from generating or leaving unauthenticated API routes, raw SQL concatenations, or exposed secrets in the environment. The agent must continuously apply this defensive posture during all implementation and review phases.

## ⚙️ Security Auditing SOP

Follow this step-by-step procedure to enforce strict security hardening:

- **Step 1: Sanitize and Validate All Input**: Implement rigorous validation schemas (e.g., Zod, JOI, or Pydantic) on every incoming API request and user form to neutralize Cross-Site Scripting (XSS) and malformed payloads.
- **Step 2: Neutralize Injection Vectors**: Reject raw string concatenation in database queries. Ensure all data access layers utilize strict parameterized queries, prepared statements, or secure ORMs to block SQL injections.
- **Step 3: Enforce Authentication and Authorization**: Audit API endpoints to guarantee that sensitive routes are protected by robust authentication middleware (JWT, OAuth) and strict Role-Based Access Control (RBAC) checks.
- **Step 4: Secure Secrets Management**: Verify that absolutely no API keys, tokens, or PII are hardcoded in the source files. Ensure all secrets are loaded dynamically via secure environment variables.
- **Step 5: Apply Safe Cross-Origin and Header Policies**: Review application configurations to ensure strict CORS policies are enforced, and security headers (e.g., Helmet, CSP) are applied to HTTP responses.
- **Step 6: Document Security Posture**: Highlight the specific security measures, validation logic, and authorization guardrails implemented in the technical walkthrough to provide a verifiable audit trail.