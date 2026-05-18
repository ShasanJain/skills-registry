---
name: narration_skill
description: Use when executing narration_skill protocols within the production sector.
---

# Narration_Skill: Execution Protocol

## ⚙️ Overview
This protocol defines the exact standards for implementing Narration_Skill. By following this strict operational pattern, the engine guarantees deterministic execution, high performance, and complete adherence to all architectural guardrails established by the system design.

# Narration Skill

Convert text to human-like speech using the `edge-tts` engine.

## Usage
- **Input**: Text string, Voice ID.
- **Output**: MP3 file in `.tmp/narration/` or specified path.

## Global Standard Voices
- `en-US-ChristopherNeural`: Neutral Male (Global standard).
- `en-US-AriaNeural`: Professional Female.
- `en-GB-RyanNeural`: British Male.

## Indian English (Hinglish Support)
- `en-IN-PrabhatNeural`: Indian Male.
- `en-IN-NeerjaNeural`: Indian Female.

## Regional Indian Voices
- **Hindi**: `hi-IN-MadhurNeural` (M), `hi-IN-SwaraNeural` (F).
- **Gujarati**: `gu-IN-NiranjanNeural` (M), `gu-IN-DhwaniNeural` (F).
- **Tamil**: `ta-IN-ValluvarNeural` (M), `ta-IN-PallaviNeural` (F).
- **Telugu**: `te-IN-MohanNeural` (M), `te-IN-ShrutiNeural` (F).

## Tool
`execution/video_audio.py`
