---
title: "Jev — TypeSafe AI's System One Decision Model"
tags:
  - AI
  - ai-agents
  - agentic-workflows
  - automation
  - tools
  - classification
  - reference
  - actionable
  - ai-tools
type: reference
status: evergreen
priority: high
date: 2026-09-21
company: TypeSafe AI
founder: Diogo Almeida
website: https://typesafe.ai
blog: https://typesafe.ai/blog/introducing-system-one-models-and-jev
launched: 2026-09-15
video_source: https://youtu.be/2mtn-Qp59y4
video_title: "15分鐘認識 Jev,做AI 自動化一定要 知道的新模型"
---

# Jev — TypeSafe AI's System One Decision Model

## Overview

**Jev** is a new category of AI model from **TypeSafe AI**, a startup founded by **Diogo Almeida** (co-author of the InstructGPT paper that underpins ChatGPT; $40M funded). TypeSafe calls it a **"System One" model** — named for Kahneman's fast, intuitive System 1 thinking, as opposed to an LLM's slow, generative "System 2" reasoning.

**Core idea:** Jev doesn't write text. It's transformer-based but outputs one of three typed decisions instead:
- a **yes/no** with a calibrated confidence score
- a **category pick** from a defined list
- a **numeric score** on a scale

Feed it context + a decision spec; it returns a structured, calibrated answer a program can act on directly — no parsing free-form text, no prompt-engineering a JSON schema out of an LLM.

## Why It's Different From an LLM

| | LLM (e.g. Claude, GPT) | Jev (System One) |
|---|---|---|
| Output | Free-form text | Typed decision (bool / category / score) |
| Strength | Reasoning, generation, nuance | Speed, cost, calibration at scale |
| Latency | Seconds | ~0.1s |
| Cost | $ per call | Fraction of a cent per call |
| Use it for | The judgment call | The triage before/around the judgment call |

**Training method:** RLCD (reinforcement learning for calibrated decisions) — optimizes directly for well-calibrated confidence, not fluent text.

## Performance

- **40–200x faster inference** than frontier LLMs on classification-shaped tasks
- **Up to 400x lower cost**
- Decisions in ~0.1s for a fraction of a cent
- Adopted within 3 days of launch by **Vercel, Cloudflare, LangChain, Langfuse**

## Access — Cloudflare Workers AI (fastest path, no waitlist)

TypeSafe's own API needs a waitlist signup. **Skip it** if you already have a Cloudflare account — Jev is available directly through **Cloudflare Workers AI**, billed to your existing account, no new secret required.

- **Model id**: `typesafe/jev`
- **From a Worker**:
  ```js
  const result = await env.AI.run('typesafe/jev', { state, questions });
  ```
- **Direct REST**:
  ```bash
  curl -X POST "https://api.cloudflare.com/client/v4/accounts/${ACCOUNT_ID}/ai/run" \
    -H "Authorization: Bearer ${CLOUDFLARE_API_TOKEN}" \
    -H "Content-Type: application/json" \
    -d '{
      "model": "typesafe/jev",
      "input": { "state": "<context to decide on>", "questions": [ /* Choice / Score / Noul spec */ ] }
    }'
  ```
- **Response**: answers come back wrapped in `result`, typed per question (Choice / Score / Noul) with calibrated probabilities.

**Other providers** (TypeSafe direct API, Vercel AI Gateway) exist too, each with its own credentials and model-id format. **Provider selection is always explicit, never auto-detected** — pick one deliberately (Cloudflare, here) rather than relying on fallback behavior.

## Best-Fit Use Cases

- **AI automation / agent workflows** — cheap gate decisions before escalating to an LLM
- **Real-time applications** needing fast decisions
- **AI map-reduce jobs** — classifying large corpora at scale
- **Verification of AI inputs/outputs** — sanity-checking another model's output
- **Model harnesses** — routing, retry logic, confidence-gated escalation

**Rule of thumb:** if a step in your pipeline is really "yes/no", "which bucket", or "how good on a 1–5 scale" — and today you're spending a full LLM call on it — that step is a Jev candidate.

## Key Takeaways

- Jev is a **decision-only** model, not a chatbot — it has no place where you need prose, explanation, or creativity.
- Its value is **economic and architectural**: it lets you keep LLM calls for the parts of a pipeline that actually need judgment/generation, and offload the high-volume filtering/classification/triage layer to something 40–200x cheaper and faster.
- The natural pattern is **Jev-as-gatekeeper**: Jev decides *whether* something is worth an expensive LLM call; the LLM only runs on what survives the gate.
- Brand new (launched 2026-09-15) — expect API/SDK details to move fast; verify current docs at [typesafe.ai](https://typesafe.ai) before building.

## Skill Candidate — `jev-gate`

Runnable today via Cloudflare (no TypeSafe waitlist dependency). Draft `SKILL.md` scaffold — drop into `.agents/skills/jev-gate/SKILL.md` as-is:

```markdown
---
name: jev-gate
description: Insert a Jev decision-gate in front of an expensive LLM step — use when a pipeline step is really a yes/no, category-pick, or score, and is currently spending a full LLM call on it.
---

## Prerequisites
- Cloudflare account with Workers AI enabled — `CLOUDFLARE_ACCOUNT_ID` + `CLOUDFLARE_API_TOKEN` (no separate TypeSafe key needed; see `notes/jev-typesafe-ai-system-one-model.md#access--cloudflare-workers-ai-fastest-path-no-waitlist`).

## When to use
Triggered when the task is: "add triage/filtering before this LLM call", "this classification step is too slow/expensive", or "reduce LLM calls in this pipeline".

## Steps
1. Identify the decision shape needed at this pipeline step: boolean (Noul), category (Choice — list the categories), or score (Score — define the scale).
2. Define what "state" Jev needs to see to make that decision (the minimal input — not the full payload the downstream LLM would get).
3. Call Jev via Cloudflare Workers AI with that state + question spec:
   ```bash
   curl -X POST "https://api.cloudflare.com/client/v4/accounts/${CLOUDFLARE_ACCOUNT_ID}/ai/run" \
     -H "Authorization: Bearer ${CLOUDFLARE_API_TOKEN}" \
     -H "Content-Type: application/json" \
     -d "{\"model\": \"typesafe/jev\", \"input\": {\"state\": \"$STATE\", \"questions\": $QUESTIONS_JSON}}"
   ```
   Read back the typed decision + confidence from `result`.
4. Set a confidence threshold: below threshold, either fall back to the LLM (don't guess) or route to human review — never silently drop on low confidence.
5. Only pass items that clear the gate on to the existing expensive step (LLM call, human review, downstream automation).
6. Log gate decisions (item, decision, confidence) for later threshold tuning — a gate with no feedback loop drifts stale.

## Completion criterion
The expensive step's call volume is measurably reduced, gate decisions are logged, and low-confidence items have an explicit fallback path (never a silent drop).
```

## Related

- [[wiki/ai-tools/ai-tools|AI Tools]]
- Candidate integration: yt-digester's classifier (see analysis note — `notes/yt-digester-jev-candidate-review.md`)

## Source

- Video: [15分鐘認識 Jev,做AI 自動化一定要 知道的新模型](https://youtu.be/2mtn-Qp59y4)
- [Introducing System One Models & Jev — TypeSafe AI Blog](https://typesafe.ai/blog/introducing-system-one-models-and-jev)
- [A new kind of AI model from a ChatGPT inventor is thrilling developers — TechCrunch](https://techcrunch.com/2026/09/18/a-new-kind-of-ai-model-from-a-chatgpt-inventor-is-thrilling-developers/)
- [Meet Jev — TechSpot](https://www.techspot.com/article/3172-meet-jev/)
- [AI model "Jev" to make machines decide faster — heise online](https://www.heise.de/en/news/AI-model-Jev-to-make-machines-decide-faster-11457071.html)

---

**Captured**: 2026-09-21
