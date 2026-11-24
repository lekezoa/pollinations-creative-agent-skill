---
name: pollinations-creative-studio
description: Generates creative multi-modal art, audio soundscapes, and concept videos using Pollinations AI models and polli CLI.
version: 1.0.0
author: lekezoa
license: MIT
metadata:
  framework: agentskills
  tags: [pollinations, generative-art, tts, soundscape, creative-agent]
---

# Pollinations Creative Studio Agent Skill

An autonomous agent skill following the [AgentSkills.io](https://agentskills.io) specification that enables coding agents (Claude Code, Codex, Hermes, OpenCode) to compose creative multi-modal artifacts—visual concept art, ambient soundscapes, voiceover tracks, and animated storyboards—using Pollinations AI generative models.

## Capabilities

1. **AI Visual Concept Generation:**
   - Synthesizes 4K/HD digital concept art, pixel game sprites, and graphic assets via Pollinations image endpoints (`flux`, `z-image-turbo`).
2. **Ambient Soundscapes & Voiceover Synthesis:**
   - Generates character voiceovers and audio narration via `openai/gpt-audio-mini` or `openai/tts-1`.
3. **Multi-Modal Scene Compositor:**
   - Combines generated imagery with synchronized voiceover into short creative media previews via standard FFmpeg automation.

## Authentication & Sign-in

Users and autonomous agents authenticate with Pollinations using the official device login flow:

```bash
# Non-interactive device authentication
npx @pollinations/cli auth login --no-browser
```

The CLI outputs the verification URL (`https://enter.pollinations.ai/device?user_code=...`) where the user signs in with their Pollinations account. For web interfaces, users authenticate via the official Pollinations OAuth `/authorize` link or the `<polli-connect>` drop-in component.

## Quick CLI Usage for Agents

```bash
# Generate creative concept art
npx @pollinations/cli image "cyberpunk neon floating pagoda at twilight" --model flux --output scene.jpg

# Generate character voiceover
npx @pollinations/cli text "Welcome traveler to the celestial realm." --model openai/gpt-audio-mini --output voice.mp3
```

## Python Integration Workflow

```python
import urllib.request
import json
import base64

def generate_scene(prompt, style="cinematic"):
    url = f"https://gen.pollinations.ai/image/{urllib.parse.quote(prompt)}?width=1920&height=1080&model=flux&seed=42"
    urllib.request.urlretrieve(url, "concept_art.jpg")
    print("Concept art saved: concept_art.jpg")

if __name__ == "__main__":
    generate_scene("A mystical ancient tree glowing with ethereal blue blossoms under a starry night sky")
```
