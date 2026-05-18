## 🛠️ Implementation SOP
Follow this step-by-step TDD procedure to execute the protocol:

- **Step 1: Baseline Context**: Verify the operational environment. Ensure required tools (like Python, Node, TS, or native CLI) are accessible before injecting new logic.
- **Step 2: Apply the Pattern**: Implement the core skill logic directly into the active system context.
- **Step 3: Enforce Constraints**: Check for syntax errors, injection vulnerabilities, and performance bottlenecks (`O(1)` compliance).
- **Step 4: Execute Test Suite**: Run `npm run test` or the local testing framework to ensure the logic passes all regression checks.
- **Step 5: Document and Commit**: Update the session walkthrough and sync the telemetry logs for the engineering sector.

---

## 📚 Reference Material

---
name: multiplayer
description: Multiplayer game development principles.
category: development
version: 4.0.5
layer: master-skill
---

# Multiplayer Game Development

> Networking architecture and synchronization principles.

---

## 1. Architecture Selection

### Decision Tree

```
What type of multiplayer?
│
├── Competitive / Real-time
│   └── Dedicated Server (authoritative)
│
├── Cooperative / Casual
│   └── Host-based (one player is server)
│
├── Turn-based
│   └── Client-server (simple)
│
└── Massive (MMO)
    └── Distributed servers
```

### Comparison

| Architecture | Latency | Cost | Security |
|--------------|---------|------|----------|
| **Dedicated** | Low | High | Strong |
| **P2P** | Variable | Low | Weak |
| **Host-based** | Medium | Low | Medium |

---

## 2. Synchronization Principles

### State vs Input

| Approach | Sync What | Best For |
|----------|-----------|----------|
| **State Sync** | Game state | Simple, few objects |
| **Input Sync** | Player inputs | Action games |
| **Hybrid** | Both | Most games |

### Lag Compensation

| Technique | Purpose |
|-----------|---------|
| **Prediction** | Client predicts server |
| **Interpolation** | Smooth remote players |
| **Reconciliation** | Fix mispredictions |
| **Lag compensation** | Rewind for hit detection |

---

## 3. Network Optimization

### Bandwidth Reduction

| Technique | Savings |
|-----------|---------|
| **Delta compression** | Send only changes |
| **Quantization** | Reduce precision |
| **Priority** | Important data first |
| **Area of interest** | Only nearby entities |

### Update Rates

| Type | Rate |
|------|------|
| Position | 20-60 Hz |
| Health | On change |
| Inventory | On change |
| Chat | On send |

---

## 4. Security Principles

### Server Authority

```
Client: "I hit the enemy"
Server: Validate → did projectile actually hit?
         → was player in valid state?
         → was timing possible?
```

### Anti-Cheat

| Cheat | Prevention |
|-------|------------|
| Speed hack | Server validates movement |
| Aimbot | Server validates sight line |
| Item dupe | Server owns inventory |
| Wall hack | Don't send hidden data |

---

## 5. Matchmaking

### Considerations

| Factor | Impact |
|--------|--------|
| **Skill** | Fair matches |
| **Latency** | Playable connection |
| **Wait time** | Player patience |
| **Party size** | Group play |

---

## 6. Anti-Patterns

| ❌ Don't | ✅ Do |
|----------|-------|
| Trust the client | Server is authority |
| Send everything | Send only necessary |
| Ignore latency | Design for 100-200ms |
| Sync exact positions | Interpolate/predict |

---

> **Remember:** Never trust the client. The server is the source of truth.
