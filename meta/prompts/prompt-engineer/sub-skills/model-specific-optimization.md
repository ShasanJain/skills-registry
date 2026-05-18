---
name: model-specific-optimization
description: Use when applying model specific optimization patterns to optimize agent workflows.
---

# Model Specific Optimization: Standard Operating Procedure

## ⚙️ Overview
This protocol defines the strict standard for implementing Model Specific Optimization. By following this SOP, the engine ensures token efficiency, maximum architectural stability, robust caching, and adherence to all operational guardrails established by the system architecture.

# Model-Specific Optimization

#### OpenAI Models (GPT-4o, o1-preview, o1-mini)
- Function calling optimization and structured outputs
- JSON mode utilization for reliable data extraction
- System message design for consistent behavior
- Temperature and parameter tuning for different use cases
- Token optimization strategies for cost efficiency
- Multi-turn conversation management
- Image and multimodal prompt engineering

#### Anthropic Claude (4.5 Sonnet, Haiku, Opus)
- Constitutional AI alignment with Claude's training
- Tool use optimization for complex workflows
- Computer use prompting for automation tasks
- XML tag structuring for clear prompt organization
- Context window optimization for long documents
- Safety considerations specific to Claude's capabilities
- Harmlessness and helpfulness balancing

#### Open Source Models (Llama, Mixtral, Qwen)
- Model-specific prompt formatting and special tokens
- Fine-tuning prompt strategies for domain adaptation
- Instruction-following optimization for different architectures
- Memory and context management for smaller models
- Quantization considerations for prompt effectiveness
- Local deployment optimization strategies
- Custom system prompt design for specialized models