# Pollinations Creative Studio Agent Skill 🎨✨

> An Agent Skill in the [AgentSkills.io](https://agentskills.io) format enabling autonomous coding agents to generate multi-modal creative art, soundscapes, and videos using Pollinations AI. Built for Pollinations AI Quest [#20020](https://github.com/pollinations/pollinations/issues/20020).

[![Made with pollinations.ai](https://raw.githubusercontent.com/pollinations/pollinations/main/packages/ui/src/brand/badge-made-with.svg)](https://pollinations.ai/?ref=badge)

---

## 🌟 Overview
This repository provides an autonomous skill definition (`SKILL.md`) for AI agents such as Claude Code, Codex, Hermes, and OpenCode. It equips agents with the procedural knowledge and CLI workflows needed to orchestrate multi-modal creative tasks—from prompt-to-artwork generation to voiceover acting and media compilation—powered by the Pollinations AI unified API and `@pollinations/cli`.

## 📁 Repository Structure
- `SKILL.md` — Formal agent skill specification with YAML frontmatter, execution workflows, and tool integrations.
- `scripts/` — Reusable helper scripts for multi-modal generation.

## 🚀 How Agents Use This Skill
Agents can install or inspect `SKILL.md` to run creative multi-modal workflows powered by `@pollinations/cli` and `gen.pollinations.ai`.

## 🔑 Sign-in & Authentication
Users and agents sign in directly with Pollinations using the official device flow:
```bash
npx @pollinations/cli auth login --no-browser
```
This opens `https://enter.pollinations.ai/device` to authorize directly with your Pollinations account. For web and browser workflows, visitors sign in with Pollinations via the official OAuth `/authorize` link (`https://enter.pollinations.ai/authorize`) or the official `<polli-connect>` drop-in component. Never requires pasting raw `sk_` keys or creating custom `pk_` App Keys.

---
Built with ❤️ for [Pollinations.ai](https://pollinations.ai).
