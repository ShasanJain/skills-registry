---
name: template-1-standard-postmortem
description: Use when executing template 1 standard postmortem protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core template 1 standard postmortem logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# Template 1: Standard Postmortem

```markdown
# Postmortem: [Incident Title]

**Date**: 2024-01-15
**Authors**: @alice, @bob
**Status**: Draft | In Review | Final
**Incident Severity**: SEV2
**Incident Duration**: 47 minutes

## Executive Summary

On January 15, 2024, the payment processing service experienced a 47-minute outage affecting approximately 12,000 customers. The root cause was a database connection pool exhaustion triggered by a configuration change in deployment v2.3.4. The incident was resolved by rolling back to v2.3.3 and increasing connection pool limits.

**Impact**:
- 12,000 customers unable to complete purchases
- Estimated revenue loss: $45,000
- 847 support tickets created
- No data loss or security implications

## Timeline (All times UTC)

| Time | Event |
|------|-------|
| 14:23 | Deployment v2.3.4 completed to production |
| 14:31 | First alert: `payment_error_rate > 5%` |
| 14:33 | On-call engineer @alice acknowledges alert |
| 14:35 | Initial investigation begins, error rate at 23% |
| 14:41 | Incident declared SEV2, @bob joins |
| 14:45 | Database connection exhaustion identified |
| 14:52 | Decision to rollback deployment |
| 14:58 | Rollback to v2.3.3 initiated |
| 15:10 | Rollback complete, error rate dropping |
| 15:18 | Service fully recovered, incident resolved |

## Root Cause Analysis