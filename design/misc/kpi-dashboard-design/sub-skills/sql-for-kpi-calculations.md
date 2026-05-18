---
name: sql-for-kpi-calculations
description: Use when executing sql for kpi calculations protocols within the design sector.
---

# Sql For Kpi Calculations: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Sql For Kpi Calculations. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core sql for kpi calculations logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the design sector.

---

## 📚 Reference Material

# SQL for KPI Calculations

```sql
-- Monthly Recurring Revenue (MRR)
WITH mrr_calculation AS (
    SELECT
        DATE_TRUNC('month', billing_date) AS month,
        SUM(
            CASE subscription_interval
                WHEN 'monthly' THEN amount
                WHEN 'yearly' THEN amount / 12
                WHEN 'quarterly' THEN amount / 3
            END
        ) AS mrr
    FROM subscriptions
    WHERE status = 'active'
    GROUP BY DATE_TRUNC('month', billing_date)
)
SELECT
    month,
    mrr,
    LAG(mrr) OVER (ORDER BY month) AS prev_mrr,
    (mrr - LAG(mrr) OVER (ORDER BY month)) / LAG(mrr) OVER (ORDER BY month) * 100 AS growth_pct
FROM mrr_calculation;

-- Cohort Retention
WITH cohorts AS (
    SELECT
        user_id,
        DATE_TRUNC('month', created_at) AS cohort_month
    FROM users
),
activity AS (
    SELECT
        user_id,
        DATE_TRUNC('month', event_date) AS activity_month
    FROM user_events
    WHERE event_type = 'active_session'
)
SELECT
    c.cohort_month,
    EXTRACT(MONTH FROM age(a.activity_month, c.cohort_month)) AS months_since_signup,
    COUNT(DISTINCT a.user_id) AS active_users,
    COUNT(DISTINCT a.user_id)::FLOAT / COUNT(DISTINCT c.user_id) * 100 AS retention_rate
FROM cohorts c
LEFT JOIN activity a ON c.user_id = a.user_id
    AND a.activity_month >= c.cohort_month
GROUP BY c.cohort_month, EXTRACT(MONTH FROM age(a.activity_month, c.cohort_month))
ORDER BY c.cohort_month, months_since_signup;

-- Customer Acquisition Cost (CAC)
SELECT
    DATE_TRUNC('month', acquired_date) AS month,
    SUM(marketing_spend) / NULLIF(COUNT(new_customers), 0) AS cac,
    SUM(marketing_spend) AS total_spend,
    COUNT(new_customers) AS customers_acquired
FROM (
    SELECT
        DATE_TRUNC('month', u.created_at) AS acquired_date,
        u.id AS new_customers,
        m.spend AS marketing_spend
    FROM users u
    JOIN marketing_spend m ON DATE_TRUNC('month', u.created_at) = m.month
    WHERE u.source = 'marketing'
) acquisition
GROUP BY DATE_TRUNC('month', acquired_date);
```