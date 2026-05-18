---
version: 1.0.0
name: video-captions
description: "Text Overlay Engine: Transcribes audio and generates dynamic on-screen captions."
---

# 💬 Video Captions: Text Overlay Engine

This skill ensures accessibility and engagement through high-impact, synchronized captions.

## 🛡️ 1. The Caption Pillars
1.  **Readability**: High-contrast text with background shadows or "letterboxing."
2.  **Chunking**: Display 3-5 words at a time to match natural speech patterns.
3.  **Emphasis**: Use color or scale to highlight key words (e.g., "URGENT" in red).
4.  **Synchronization**: Precise timing (SRT format) aligned with the audio waveform.

## 🏗️ 2. Industrial Caption Protocol
- **Transcription**: Convert speech to text using Whisper or Deepgram.
- **Styling**: Modern, bold sans-serif fonts.
- **Animation**: Subtle pop-in or slide-up effects.

## ⌨️ Commands
| Command | Action |
| :--- | :--- |
| `/video-captions [audio_path]` | Calls `video_captions.py` to generate SRT and styling JSON. |

---
*Status: STABLE. Pattern: Industrial.*
