---
name: cicd-secret-scanning
description: Use when executing cicd secret scanning protocols within the security sector.
---

# Cicd Secret Scanning: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Cicd Secret Scanning. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# CI/CD Secret Scanning

```yaml
secret-scan:
  stage: security
  image: trufflesecurity/trufflehog:latest
  script:
    - trufflehog filesystem .
  allow_failure: false
```

## Reference Files

- `references/vault-setup.md` - HashiCorp Vault configuration
- `references/github-secrets.md` - GitHub Secrets best practices

## Related Skills

- `github-actions-templates` - For GitHub Actions integration
- `gitlab-ci-patterns` - For GitLab CI integration
- `deployment-pipeline-design` - For pipeline architecture