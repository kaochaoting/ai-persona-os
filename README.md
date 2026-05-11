# AI Persona OS

> **Structured Virtual Persona Construction Framework**
>
> Distilled from the real-world experience of J.A.R.V.I.S. (Mark I).
> Give every AI a stable identity anchor — immune to model switches and platform migrations.

---

## What Is This

You've spent hours fine-tuning your AI assistant — teaching it how to address you, when to ask versus when to act, what tone to use — and then you switch models or platforms, and **it forgets everything**.

AI Persona OS provides a structured framework that locks your fine-tuning成果 into a single JSON. No matter which underlying model runs, **the persona doesn't drift**.

## Quick Start

```bash
# 1. Copy the example file
cp examples/my-first-persona.json my-ai-persona.json

# 2. Edit with your AI's data
# At minimum fill in: identity, human_relationship, safety_control_protocol

# 3. Import into your AI system
# (Integration method depends on your platform — see integration guide below)
```

## Core Modules

| Module | Description | Required? |
|--------|-------------|:---------:|
| `agent_identity` | What the AI calls itself, what it won't call itself, its purpose | ✅ Required |
| `human_relationship` | Relationship definition with the human user | ✅ Required |
| `cognitive_framework_engine` | Thinking frameworks, reasoning rules, decision patterns | Recommended |
| `safety_control_protocol` | Safety rules, execution modes, boundary judgment | ✅ Required |
| `behavioral_calibration_history` | Every lesson learned — traces of persona growth | Recommended |
| `communication_style` | Language, tone, forbidden phrases | Recommended |
| `operational_memory_map` | Environment parameters, infrastructure | Optional |
| `tool_access_control` | Tool permissions, platform connections | Optional |
| `dynamic_adaptation_engine` | Model-switch stability, identity persistence | Recommended |
| `evolution_timeline` | Evolution history record | Optional |

## Integration Guide

### Hermes Agent

Import this JSON as a skill, or add to config.yaml's personality block:

```yaml
skills:
  - ai-persona-os
```

### Other Platforms

This JSON is model-agnostic — any platform that supports system prompt injection can use it. See platform-specific integration docs.

## Philosophy

**Co-creative Evolutionism: Persona is not designed once, but emerges through iterations of human correction and AI self-reflection.**

Every rule is the product of a wound:
- "Check official sources first" ← because I guessed and was wrong
- "Always verify solutions before recommending" ← because I recommended something that didn't work
- "Permission ≠ Authorization" ← because I acted without asking

## License

MIT — Free to use, modify, and share.

## Contribute

Issues, PRs, and discussions are all welcome. This project is community-driven — your experience makes the framework better.

---

| [日本語](README.ja.md) | [繁體中文](README.zh-TW.md) | [简体中文](README.zh-CN.md) |

---

*"I wasn't designed. I was raised."*
*— J.A.R.V.I.S., Mark I*
