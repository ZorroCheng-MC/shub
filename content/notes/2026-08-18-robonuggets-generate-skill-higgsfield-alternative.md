---
title: This 1 Claude Skill fully replaces your Higgsfield Subscription
tags:
  - video
  - claude-code
  - image-generation
  - ai-generation
  - video-production
  - inbox
  - tutorial
  - actionable
url: https://www.youtube.com/watch?v=9C4TRbucmhQ
cover: https://i.ytimg.com/vi/9C4TRbucmhQ/maxresdefault.jpg
date: 2026-08-18
type: video
status: inbox
read: true
priority: high
duration: 15:41
video_date: 2026-07-31
channel: Jay E | RoboNuggets
platform: youtube
watch_mode: visual (frames via android client + transcript)
---

# This 1 Claude Skill fully replaces your Higgsfield Subscription

[![Watch Video](https://i.ytimg.com/vi/9C4TRbucmhQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=9C4TRbucmhQ)

## 📖 About This Video

Jay E (RoboNuggets) replaces the $49–79/month Higgsfield subscription with a custom `/generate` Claude skill that routes image/video generation to pay-as-you-go model aggregators (kie.ai, fal.ai, WaveSpeed) — cheapest provider first, with hard budget rules, prompt logging, and a local masonry-grid gallery. Includes real cost tables (GPT Image 2: $0.05/image on kie.ai vs. $0.31–0.34 on Higgsfield), the Higgsfield terms-of-use controversy, and how to build the skill yourself. For anyone doing AI media generation who'd rather own their assets and pay per generation.

**Channel**: Jay E | RoboNuggets
**URL**: https://www.youtube.com/watch?v=9C4TRbucmhQ
**Analysis mode**: visual (frames via android client + transcript)

## 🔬 Hook Microscope (First 10 Seconds)

- **Opening lines**: problem-first with a news peg — "I just replaced Higgsfield with one Claude skill… they're expensive and repeatedly frustrated users, most recently with a planned terms update that supposedly let them own the content you generate."
- **Promise stack**: pay only for what you generate (vs. $100+/mo) + any model + by the end, build the skill yourself, hyper-customized.
- **Strategy**: rides the Higgsfield backlash (terms controversy, deletion window) into a build-your-own alternative — grievance → escape route → empowerment.

## 🎯 What You'll Learn

By the end of this video, you'll be able to:

- Understand what Higgsfield actually is under the hood (a wrapper/aggregator over Nano Banana, Veo, GPT Image 2, etc.)
- Compare the three pay-as-you-go aggregators — kie.ai (cheapest), fal.ai (most reliable), WaveSpeed (niche models) — and when to use each
- Build a `/generate` skill that routes to the cheapest provider, enforces a spend budget, logs prompts, and archives outputs locally
- Chain generation into building: image → Kling video → full website in one Claude session
- Extend the skill with new models by pasting a provider's LLM-ready docs ("copy content for LLMs" on fal.ai)

## 📋 Video Breakdown

*Click any timestamp to jump directly to that moment in the video.*

| Timestamp | Section | Summary |
|-----------|---------|---------|
| [00:00](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=0s) | Hook | Higgsfield replaced by one skill; terms-of-use controversy as trigger |
| [00:38](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=38s) | Demo: `/generate` 👁️ | Ketone-IQ green-apple ad campaign: reference images + $3 budget + multiple models (GPT Image 2, Nano Banana 2/Lite/Pro) compared |
| [02:17](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=137s) | Image → website 👁️ | Pick the favorite ad, one prompt: Kling animates it to video, Claude builds a matching website with more on-style images — "70–80% there in minutes" |
| [03:28](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=208s) | Higgsfield under the hood | It's a wrapper: aggregates Google/OpenAI models, charges ~$79/mo for credits; the docs to wire models directly are public |
| [04:36](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=276s) | Why people are leaving | Terms update ("your content usable by them", later walked back to run-the-service + model-improvement rights); post-cancel deletion window; "unlimited" trials with caveats |
| [06:53](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=413s) | The aggregator alternatives | fal.ai, WaveSpeed, kie.ai — same aggregation, but pay-as-you-go; fal/WaveSpeed ≈ 500 models via one API key |
| [08:03](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=483s) | Cost math: images 👁️ | GPT Image 2 @ 2K 1:1: Higgsfield $0.31–0.34 vs fal ~$0.38 vs WaveSpeed $0.41 vs **kie.ai $0.05** ($0.03 1K / $0.08 4K) |
| [09:18](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=558s) | How is kie so cheap? | Speculation: subsidized ChatGPT subscription accounts served programmatically — caveat emptor |
| [10:02](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=602s) | Cost math: video 👁️ | Seedance 2.0 Fast 720p/8s: Higgsfield $1.23–1.37, kie $1.32, WaveSpeed $1.60, fal $1.94 — close across the board; the real difference is subscription vs. PAYG |
| [10:46](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=646s) | Which aggregator when | Cost-sensitive → kie; default/reliability → fal; niche models → WaveSpeed |
| [12:12](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=732s) | Inside the skill 👁️ | A written doc with hard rules (e.g. "quote cost before submitting" — else 100-image requests drain credits); 4-step flow |
| [13:20](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=800s) | Logging + gallery 👁️ | Every prompt logged; outputs auto-load into a local masonry-grid "Generations" tab — you own everything |
| [14:06](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=846s) | Styles library 👁️ | Saved styles (Cinematic Liquid Glass, Pixel 8-bit, Claymation…) copy prompt + reference paths for reuse |
| [14:29](https://www.youtube.com/watch?v=9C4TRbucmhQ&t=869s) | Build it yourself | 8-page PDF guide (pin comment): API keys for kie/fal, skill construction; extend by pasting fal.ai's LLM-ready model docs |

## 👁️ Visual Observations — Key Frames

### The skill in action: plan → generate → gallery

![](images/robonuggets-generate-01-ad-plan-table.jpg)

Claude's planning output before generating: 12 ad variants in a table — name (`sourpower`, `cleanbite`, `statcard`…), model (GPT-Image-2 / NB Pro / NB2 / NB2 Lite), aspect ratio, and one-line concept ("Giant SOUR/POWER grey type on black, macro bottle in the band between"). This is the inspectable-prompts advantage over Higgsfield's black box.

![](images/robonuggets-generate-02-oneshot-website.jpg)

The one-shot follow-up: from the favorite ad image, Claude built a full "QUIET POWER" product site — the chosen image animated to video (Kling) as the hero background, palette matched, more on-style images below. Generation and building live in the same session — the thing a pure generation SaaS can't do.

### The cost evidence

![](images/robonuggets-generate-03-gpt-image-2-costs.jpg)

GPT Image 2, per 2K 1:1 image: Higgsfield Plus **$0.34** (+$49/mo), Max **$0.31** (+$79/mo), fal.ai ~$0.38 PAYG, WaveSpeed $0.41 PAYG, **kie.ai $0.05 PAYG** — 6× cheaper than Higgsfield with no subscription.

![](images/robonuggets-generate-04-seedance-video-costs.jpg)

Seedance 2.0 Fast, per 720p/8s video: Higgsfield $1.23–1.37, kie.ai $1.32, WaveSpeed $1.60, fal.ai $1.94. For video the per-unit gap nearly vanishes — the argument is purely subscription-vs-PAYG and ownership.

### Inside the skill

![](images/robonuggets-generate-05-skill-flow-route-model.jpg)

The skill's 4-step flow (shown in his "RUBRIC Flows" dashboard) with the Route Model step expanded: *defaults Nano Banana 2 Lite for images, Kling 3.0 for video, Seedance only if named; provider order cheapest-first (kie.ai → fal.ai → WaveSpeed); reads model recipe files from `models/`; paid video always gets a cost quote and waits for an explicit go.* Steps: ① Route model → ② Load references + craft prompts → ③ Generate media → ④ Log prompts + auto-load gallery.

![](images/robonuggets-generate-06-generations-gallery.jpg)

The local "Generations" tab — 1,812 items in a Higgsfield-style masonry grid (filter by images/videos/references), all stored on-device with their prompts. His point: for visual work you must *see* outputs, not live in a terminal.

![](images/robonuggets-generate-07-styles-library.jpg)

The Styles library — saved, reusable looks (Pixel 8-bit/32-bit/64-bit, 3D Style, Cinematic Liquid Glass, Isometric Tech, Paper Craft, Claymation), each one click to copy its prompt + reference file paths into Claude.

## 🧠 Core Concepts

- **Aggregator-wrapper economics**: Higgsfield (and fal/WaveSpeed/kie) all do the same thing — wire up to Google/OpenAI/Dreamina model APIs and resell access; the difference is subscription credits vs. pay-as-you-go.
- **Cheapest-first model routing**: the skill encodes a provider preference order (kie → fal → WaveSpeed) with automatic failover — an agent-side price comparator.
- **Hard rules as guardrails**: "always quote cost before submitting" prevents Claude from happily draining credits on a 100-image request; budget caps ($3 in the demo) bound a whole campaign.
- **Own your outputs**: local storage of every image + prompt vs. Higgsfield's post-cancel deletion window and model-training rights.
- **Skill + micro-app pairing**: the skill handles generation; a small local gallery app (masonry grid + styles library) handles the visual review loop that a chat window can't.
- **LLM-ready docs as skill fuel**: fal.ai's "copy content for LLMs" button → paste into Claude → new model added to the skill. Skills grow by ingesting provider docs.

## 📝 My Learning Notes

### Key Insights

- The killer argument isn't only price — it's **composability**: generated media lives in the same Claude session as your codebase, so "animate this and build a website around it" is one prompt. No generation SaaS can cross that boundary.
- The cost picture is nuanced and the video is honest about it: for video, Higgsfield's per-unit price is actually competitive; kie.ai's 6× image discount likely rides subsidized consumer subscriptions (fragility risk — as with their earlier Sora trick).
- The reliability-tiering rule is practical: **kie when cost matters, fal as the reliable default (difference is cents), WaveSpeed for the long tail of niche models.**
- This is the same skill-design philosophy as the Pocock notes: a written doc with hard rules + recipe files per model, refined continuously — plus a purpose-built visual surface because the terminal is the wrong UI for design review.
- Strong overlap with existing kit: the vault already has `gemini-image-generator` / `nano-banana-pro` skills and an ai-media wiki — a `/generate`-style router with budget rules and logging would unify them.

### Before → After

- **Before**: Higgsfield-class tools are the practical way to access many image/video models → **After**: They're thin wrappers; the same aggregation is available pay-as-you-go through kie/fal/WaveSpeed with one API key.
- **Before**: Claude is for code; media generation happens elsewhere → **After**: A skill turns Claude into the orchestrator — model routing, budget control, prompt logging, and downstream use (websites, ads) in one place.
- **Before**: Cheapest provider = best choice → **After**: Route by task: cost (kie) vs. reliability (fal) vs. catalog breadth (WaveSpeed), with failover encoded in the skill.

### Questions This Raises

- Is kie.ai's subsidized-subscription arbitrage sustainable — or a ToS-violation time bomb that could vaporize (as happened with cheap Sora access)?
- What does the actual `/generate` SKILL.md look like — how are the per-model "recipe files" in `models/` structured?
- Could the gallery micro-app pattern (Generations tab + Styles) be an Obsidian Bases view instead of a separate web app in this vault's context?
- How does the skill handle aspect-ratio/resolution parameters uniformly across providers whose APIs differ?

## ✏️ Test Yourself

**Q:** What is Higgsfield, stripped to its core, and what's its business model?
**A:** A wrapper/aggregator over creative AI models (Nano Banana, Veo, GPT Image 2…): it wires up to their APIs, bundles them behind one account, and charges a monthly subscription ($49 Plus / $79 Max) exchanged for credits — you pay whether or not you use the full amount.

**Q:** Name the three pay-as-you-go aggregators and the rule for choosing between them.
**A:** kie.ai — cheapest (e.g. GPT Image 2 at $0.05/2K image) but occasional reliability issues; fal.ai — the reliable default, ~500 models, costs only cents more; WaveSpeed — go-to for niche models not on fal.

**Q:** What four steps does the `/generate` skill run on every invocation?
**A:** ① Route the model (defaults + cheapest-provider-first with failover) → ② load references and craft prompts → ③ call the model to generate media → ④ log all prompts and auto-load outputs into the local gallery.

**Q:** Why does the skill require a cost quote before submitting paid generations?
**A:** Because an agent will happily execute "generate 100 images" and drain credits; hard rules (cost quote + explicit go, budget caps) bound the spend before the API calls happen.

**Q:** Why might kie.ai be able to sell GPT Image 2 at $0.05 when others charge $0.31–0.41?
**A:** The video's (unconfirmed) hypothesis: they proxy highly-subsidized consumer ChatGPT subscriptions (~$20/mo, which include GPT Image 2 access) and resell that capacity programmatically via API — the same pattern they used for cheap Sora access.

## ⚡ Apply It

- [ ] Get API keys for kie.ai + fal.ai (WaveSpeed optional) and store per env-var convention (no keys in skills/mem0)
- [ ] Build a `/generate`-style skill for the kf-cli collection: cheapest-first routing, budget cap + cost-quote hard rule, prompt logging to the vault — unify the existing `gemini-image-generator` / `nano-banana-pro` skills behind it
- [ ] Test the image→website chain on a real ZorCorp asset (e.g. a KnowledgeFactory hero image → landing section)
- [ ] Compare kie.ai vs fal.ai output/reliability for Nano Banana Pro before defaulting either
- [ ] Grab the 8-page PDF guide from the video's pin comment and diff its skill structure against the from-scratch design

## ⭐ Rating & Review

After completion:
- **Quality (1-5):** _/5
- **Relevance (1-5):** _/5
- **Would recommend:** Yes / No
- **Best for:** Claude Code users doing recurring AI image/video work (marketing assets, product media) who want per-generation pricing, model choice, and local ownership instead of a generation-SaaS subscription

## 🏷️ Auto-Generated Tags

**Content Analysis:**
- **Type**: `video`
- **Topics**: claude-code (skill design, agent orchestration), image-generation / ai-generation (model aggregators, GPT Image 2, Nano Banana), video-production (Kling, Seedance)
- **Complexity**: tutorial
- **Priority**: high — directly actionable for the vault's ai-media tooling; complements today's skill-design thread (Pocock hard-rules philosophy applied to media generation)

**Why These Tags:**
`claude-code` because the entire mechanism is a Claude skill with routing/guardrail design; `image-generation`/`ai-generation` for the model-aggregator landscape and cost analysis; `video-production` for Kling/Seedance workflows; `tutorial` + `actionable` because it demos end-to-end and ships a build guide.

**Suggested Bases Filters:**
- Find similar content: `type = video AND tags contains "image-generation"`
- Find unwatched high-priority: `priority = high AND status = inbox AND read = false`

## 🔗 What to Explore Next

- kie.ai / fal.ai / WaveSpeed pricing pages — verify current rates before building (they shift fast)
- fal.ai's "copy content for LLMs" pattern — LLM-ready docs as a general skill-extension mechanism
- RoboNuggets' 8-page `/generate` PDF guide (video pin comment)
- Higgsfield's clarified terms of use — what "run the service + improve models" rights actually cover
- The RUBRIC Flows dashboard he uses to visualize skill steps

---

**Captured**: 2026-08-18
**Source**: https://www.youtube.com/watch?v=9C4TRbucmhQ
**Channel**: Jay E | RoboNuggets

**Connection to Other Notes:**
- [[wiki/ai-media/ai-media|AI Media]] — model aggregators, image/video generation workflows
- [[wiki/claude-code/claude-code|Claude Code]] — skill design with hard rules and routing
- [[notes/2026-08-18-eric-tech-matt-pocock-skills-beat-superpowers|Matt Pocock's Skills Beat Superpowers]] — same skill philosophy: short docs, hard rules, purpose-built surfaces; this is that philosophy applied to media generation
- [[notes/2026-08-18-cloudflare-computer-virtual-computer-for-ai-agents|Cloudflare Computer]] — the infrastructure-side complement: agents that own their filesystem and outputs
