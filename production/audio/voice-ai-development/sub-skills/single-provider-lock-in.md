---
name: single-provider-lock-in
description: Use when executing single provider lock in protocols within the production sector.
---

# Single Provider Lock In: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Single Provider Lock In. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# ❌ Single Provider Lock-in

**Why bad**: May not be best quality.
Single point of failure.
Harder to optimize.

**Instead**: Mix best providers:
- Deepgram for STT (speed + accuracy)
- ElevenLabs for TTS (voice quality)
- OpenAI/Anthropic for LLM

## Limitations

- Latency varies by provider
- Cost per minute adds up
- Quality depends on network
- Complex debugging

## Related Skills

Works well with: `langgraph`, `structured-output`, `langfuse`