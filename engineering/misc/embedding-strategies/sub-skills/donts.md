---
name: donts
description: Use when executing donts protocols within the engineering sector.
---

# Donts: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Donts. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Don'ts

- **Don't ignore token limits** - Truncation loses info
- **Don't mix embedding models** - Incompatible spaces
- **Don't skip preprocessing** - Garbage in, garbage out
- **Don't over-chunk** - Lose context

## Resources

- [OpenAI Embeddings](https://platform.openai.com/docs/guides/embeddings)
- [Sentence Transformers](https://www.sbert.net/)
- [MTEB Benchmark](https://huggingface.co/spaces/mteb/leaderboard)