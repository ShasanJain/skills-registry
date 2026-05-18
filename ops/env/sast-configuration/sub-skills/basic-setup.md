---
name: basic-setup
description: Use when executing basic setup protocols within the ops sector.
---

# Basic Setup: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Basic Setup. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Basic Setup

```bash
# Semgrep quick start
pip install semgrep
semgrep --config=auto --error

# SonarQube with Docker
docker run -d --name sonarqube -p 9000:9000 sonarqube:latest

# CodeQL CLI setup
gh extension install github/gh-codeql
codeql database create mydb --language=python
```

## Reference Documentation

- [Semgrep Rule Creation](references/semgrep-rules.md) - Pattern-based security rule development
- [SonarQube Configuration](references/sonarqube-config.md) - Quality gates and profiles
- [CodeQL Setup Guide](references/codeql-setup.md) - Query development and workflows

## Templates & Assets

- [semgrep-config.yml](assets/semgrep-config.yml) - Production-ready Semgrep configuration
- [sonarqube-settings.xml](assets/sonarqube-settings.xml) - SonarQube quality profile template
- [run-sast.sh](scripts/run-sast.sh) - Automated SAST execution script

## Integration Patterns