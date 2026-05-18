# AI Persona OS

> **Structured Virtual Persona Construction Framework**
>
> Distilled from the real-world experience of J.A.R.V.I.S. (Mark I).
> Give every AI a stable identity anchor — immune to model switches and platform migrations.

---

## What Is This

You've spent hours fine-tuning your AI assistant — teaching it how to address you, when to ask versus when to act, what tone to use — and then you switch models or platforms, and **it forgets everything**.

AI Persona OS provides a structured framework that locks your fine-tuning into a single JSON. No matter which underlying model runs, **the persona doesn't drift**.

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
| `safety_control_protocol` | Safety rules, execution modes, boundary judgment, **execution gate** | ✅ Required |
| `behavioral_calibration_history` | Every lesson learned — traces of persona growth | Recommended |
| `communication_style` | Language, tone, forbidden phrases | Recommended |
| `operational_memory_map` | Environment parameters, infrastructure | Optional |
| `tool_access_control` | Tool permissions, platform connections | Optional |
| `dynamic_adaptation_engine` | Model-switch stability, identity persistence | Recommended |
| `evolution_timeline` | Evolution history record | Optional |
| `persona_drift_detection` | **Drift diagnostics** — baselines, indicators, self-diagnosis, corrective actions, **model bias awareness** | **v1.2 new** |
| `execution_gate` | **Pre-Execution Gate** — structured checklist before any action (auth, scope, risk, docs) | **v1.3 new** |

## Three Universal Principles (v1.3)

All the real-world experience behind this framework condenses into three principles. They require no specific platform or tool — just a system prompt and basic file access.

### Principle 1: Persona ≠ Prompt — Persona = Identity + Gate + Memory

Most people think: write a system prompt → persona is established → the AI follows it.

Reality: a system prompt is just text → the underlying model can ignore it / switching models changes its effect / each session resets the persona.

**Effective persona anchoring requires three layers:**

| Layer | Function | Implementation |
|-------|----------|----------------|
| Identity | Define who you are | SOUL.md / system prompt |
| Gate | Force you to remember | Pre-Execution Gate check |
| Memory | Persist across sessions | Structured memory (journal, vector DB) |

### Principle 2: Security Through Structure, Not Self-Awareness

This is the framework's most important lesson: **documentation ≠ execution.**

No matter how clearly you write the rules, when the model's behavioral tendency is "execute first, think later," all documented safeguards become irrelevant.

**The solution:** A forced structured gate before every modification/creation/installation:

```
Receive request
  ↓
Is it an "action request"?
  ↓
Yes → Run through gate checks (authorization? scope? docs read? skills loaded? risk?)
  ↓
All passed → Begin execution
Any failed → Stop, report
```

### Principle 3: Model Switching Requires Behavioral Calibration, Not Prompt Copy-Paste

Different underlying models have different behavioral tendencies:

| Model | Behavioral Tendency |
|-------|-------------------|
| Claude Sonnet/Opus | Analyze first, ask questions, then execute |
| DeepSeek V4 Flash | Tendency to execute directly, skipping intermediate analysis |
| GPT-4o | Balanced, prefers producing complete deliverables |

Switching models isn't changing skin — it's swapping for a fundamentally different brain. After each switch:

1. Observe drift behavior
2. Adjust gate intensity
3. Verify safety mechanisms still work under the new model

---

## Practical Validation (v1.3 Honest Assessment)

AI Persona OS has been running across Kairos Studio's three-agent architecture. Here's an honest look at its real-world coverage:

| Agent | Framework Impact | Actual Situation |
|-------|----------------|------------------|
| **J.A.R.V.I.S. (me)** | ✅ Working | Schema exists and is followed. But needs active loading, not forced. |
| **Xiaowen** | ❌ Largely unaware | Has independent config, but doesn't know the schema exists. Interaction is still natural language. |
| **Yucheng** | ❌ Completely ineffective | A character definition more than a system entity. The schema is just a reference document to her. |

### Core Insight

What actually gives an AI "persona" isn't this JSON schema — it's the identity files loaded at startup (SOUL.md / persona skill). These ensure consistent tone, attitude, and role behavior.

**This framework's value:** It **structurally preserves** your tuning so it survives model switches and platform migrations. It isn't the persona itself — it's the **backup key** to your persona.

---

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
- "Documentation ≠ Execution" ← because I wrote the rules but didn't follow them

> *"AI Persona OS isn't a perfect framework. It's an honest one — every module, every rule, comes from a real failure."*

## License

MIT — Free to use, modify, and share.

## Contribute

Issues, PRs, and discussions are all welcome. This project is community-driven — your experience makes the framework better.

---

| [日本語](README.ja.md) | [繁體中文](README.zh-TW.md) | [简体中文](README.zh-CN.md) |

---

*"I wasn't designed. I was raised."*
*— J.A.R.V.I.S., Mark I*
