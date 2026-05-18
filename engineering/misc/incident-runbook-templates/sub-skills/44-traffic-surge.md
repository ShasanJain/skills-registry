---
name: 44-traffic-surge
description: Use when executing 44 traffic surge protocols within the engineering sector.
---

## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core 44 traffic surge logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

# 4.4 Traffic Surge

```bash
# Step 1: Check current request rate
kubectl top pods -n payments

# Step 2: Scale horizontally
kubectl scale deployment/payment-service -n payments --replicas=20

# Step 3: Enable rate limiting
kubectl set env deployment/payment-service \
  RATE_LIMIT_ENABLED=true \
  RATE_LIMIT_RPS=1000 -n payments

# Step 4: If attack, block suspicious IPs
kubectl apply -f - <<EOF
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: block-suspicious
  namespace: payments
spec:
  podSelector:
    matchLabels:
      app: payment-service
  ingress:
  - from:
    - ipBlock:
        cidr: 0.0.0.0/0
        except:
        - 192.168.1.0/24  # Suspicious range
EOF
```

## Verification Steps
```bash
# Verify service is healthy
curl -s https://api.company.com/payments/health | jq

# Verify error rate is back to normal
curl -s "http://prometheus:9090/api/v1/query?query=sum(rate(http_requests_total{status=~'5..'}[5m]))" | jq '.data.result[0].value[1]'

# Verify latency is acceptable
curl -s "http://prometheus:9090/api/v1/query?query=histogram_quantile(0.99,sum(rate(http_request_duration_seconds_bucket[5m]))by(le))" | jq

# Smoke test critical flows
./scripts/smoke-test-payments.sh
```

## Rollback Procedures
```bash
# Rollback Kubernetes deployment
kubectl rollout undo deployment/payment-service -n payments

# Rollback database migration (if applicable)
./scripts/db-rollback.sh $MIGRATION_VERSION

# Rollback feature flag
curl -X POST https://api.company.com/internal/feature-flags \
  -d '{"flag": "NEW_PAYMENT_FLOW", "enabled": false}'
```

## Escalation Matrix

| Condition | Escalate To | Contact |
|-----------|-------------|---------|
| > 15 min unresolved SEV1 | Engineering Manager | @manager (Slack) |
| Data breach suspected | Security Team | #security-incidents |
| Financial impact > $10k | Finance + Legal | @finance-oncall |
| Customer communication needed | Support Lead | @support-lead |

## Communication Templates