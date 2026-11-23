---
title: 1:1复刻视频？火爆Github！这个ai逆向视频的工具太强了 | 手把手教你使用 rea video
tags:
  - video
  - ai
  - open-source
  - video-production
  - inbox
  - tutorial
  - actionable
url: https://www.youtube.com/watch?v=Nlg7hKPPkSw
cover: https://i.ytimg.com/vi/Nlg7hKPPkSw/maxresdefault.jpg
date: 2026-11-20
type: video
status: inbox
read: true
priority: medium
duration: 4:44
video_date: 2026-11-07
channel: ITCoderGao
platform: youtube
watch_mode: transcript-only (no captions; local Whisper "small" transcription, zh)
---

# 1:1复刻视频？火爆Github！这个ai逆向视频的工具太强了 | 手把手教你使用 rea video

[![Watch Video](https://i.ytimg.com/vi/Nlg7hKPPkSw/maxresdefault.jpg)](https://www.youtube.com/watch?v=Nlg7hKPPkSw)

## 📖 About This Video

A short (under 5 min) Chinese-language walkthrough of **rea-video**, a trending open-source project that pairs with an AI coding agent to "reverse-engineer" any visual media (video, 3D models, effects, web animations, demos). The tool outputs a detailed analysis report, and you then ask the agent to rebuild a similar video from that report. Aimed at creators and developers who see a polished effect and want to know how it was made.

**Channel**: ITCoderGao
**URL**: https://www.youtube.com/watch?v=Nlg7hKPPkSw
**Analysis mode**: transcript-only. YouTube captions are disabled, so the audio was transcribed locally with Whisper (small, zh). Frames were not analysed. Tool/product names may be mis-transcribed; the exact GitHub repo is not given in the video text (the creator says the commands and links are in his community post).

## 🔬 Hook Microscope (First 10 Seconds)

- Title hook is a bold promise ("1:1 复刻视频", "火爆Github") plus a curiosity gap on "AI reverse-engineering video".
- Opening lines: "A project that's blowing up in open source… it works with AI to break down *everything visual* — video, 3D modelling, effects, web animation, demos."
- Strategy: **claim-first / outcome-first**. States the payoff (a plan detailed enough to remake a similar video) in the first 20 seconds, then moves straight into setup.

## 🎯 What You'll Learn

By the end of this video, you'll be able to:

- Understand what rea-video does and what its report contains
- Install the prerequisites (Python environment, FFmpeg, an AI agent) and have the agent install the project
- Run the bundled demo analysis, then analyse your own clip into an `output/` folder
- Prompt the agent to rebuild a video effect from the generated report

## 📋 Video Breakdown

*Click any timestamp to jump directly to that moment in the video.*

| Time                                                        | Segment                                                                                                            |
| ----------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| [00:00](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=0s)   | Intro: what the tool does (breaks down any visual media, outputs a plan)                                           |
| [00:31](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=31s)  | Prerequisites: Python environment, FFmpeg (video processing), an AI agent                                          |
| [00:59](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=59s)  | Agent choice: Claude Code, Codex or DeepSeek all work; use whichever you know                                      |
| [01:11](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=71s)  | Find the project on GitHub, open the agent in a project folder, paste the repo link and ask it to install          |
| [01:33](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=93s)  | Project layout: only the demo folder matters at first                                                              |
| [01:48](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=108s) | Demo run: ask the agent to analyse a demo video, saving results to `output/`                                       |
| [02:10](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=130s) | Report contents: % AI-generated vs 3D-rendered, scenes, props, sound effects, shooting method, script, remake plan |
| [02:36](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=156s) | Hands-on: recreate a card-effect video (analyse, open `report.html`)                                               |
| [03:20](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=200s) | Prompt the agent to rebuild the video from the analysis                                                            |
| [03:32](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=212s) | Result: a web front-end implementation of the effect, plus an auto-rendered video file                             |
| [04:03](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=243s) | Verdict: the clone even reproduced the source's clipped-text flaw                                                  |
| [04:25](https://www.youtube.com/watch?v=Nlg7hKPPkSw&t=265s) | Wrap-up: use it whenever you see an effect and don't know how it's made                                            |

## 👁️ Visual Observations

*What the frames revealed that the transcript alone would miss.*

*Note: visual analysis unavailable — transcript-only (no captions; local Whisper transcription).*

## 🧠 Core Concepts

- **Visual reverse-engineering**: an agent-driven tool that decomposes a video or effect into structured analysis rather than just describing it.
- **Analysis report**: a report (HTML) with the share of AI vs 3D-rendered content, scenes, props, sound design, shooting methods, script and a remake plan.
- **Agent as installer and operator**: you paste the repo link into an AI coding agent and let it install and run the project.
- **Prerequisites**: a Python environment and FFmpeg (video processing); any capable agent (Claude Code, Codex, DeepSeek).
- **Analysis → rebuild loop**: analyse a clip into `output/`, then prompt the agent to recreate it as a web-based effect, with an automatic render to a video file.

## 📝 My Learning Notes

### Key Insights

- The value is in the *report as a spec*: once a video is decomposed, a second prompt can rebuild it.
- Agent-agnostic: any coding agent that can run shell commands and read files works.
- Fidelity is high enough to copy the original's flaws (clipped text), which suggests it recreates, not just inspires.
- The creator keeps the exact prompts and links in a YouTube community post, so the video alone isn't enough to reproduce the steps.

### Before → After

- **Before**: Seeing a slick effect with no idea how it was made → **After**: Feed it to an agent and get a scene-by-scene breakdown and a rebuild plan.
- **Before**: Manual frame-by-frame study → **After**: One prompt produces a structured report and a first-draft clone.

### Questions This Raises

- What is the exact repo name and licence? (not stated in the video text)
- Which model/vision backend does the analysis use, and what does it cost per video?
- How accurate are the "% AI vs 3D-rendered" claims?
- Are there copyright concerns when cloning someone else's video or effect "1:1"?

### Personal Reflections

*Add your own notes here after watching*

## ✏️ Test Yourself

*Answer these before and after watching to measure what you learned.*

**Q:** What two tools must be installed before the agent can set up the project?
**A:** A Python environment and FFmpeg.

**Q:** Which folder should a beginner look at first in the project?
**A:** The demo folder, which has the author's sample cases.

**Q:** What kinds of detail does the generated report include?
**A:** AI vs 3D-rendered share, scenes, props, sound effects, shooting methods, script and a remake plan.

**Q:** How is the second step (rebuilding) done?
**A:** Give the agent a second prompt asking it to recreate the video from the analysis results.

## ⚡ Apply It

*Specific actions to take based on what this video teaches.*

- [x] Find the project's GitHub repo (check the video's community post / search "rea-video")
- [x] Confirm Python and FFmpeg are installed (`ffmpeg -version`)
- [x] Have Claude Code install the repo and run the bundled demo analysis
- [x] Analyse one of my own reference clips and review the generated `report.html`
- [ ] Try the rebuild prompt for a simple web animation effect

## ⭐ Rating & Review

After completion:
- **Quality (1-5):** _/5
- **Relevance (1-5):** _/5
- **Would recommend:** Yes / No
- **Best for:** Creators and developers using AI coding agents who want to deconstruct and recreate video effects

## 🏷️ Auto-Generated Tags

**Content Analysis:**
- **Type**: `video`
- **Topics**: ai, open-source, video-production — agent-driven open-source tooling applied to video analysis and recreation
- **Complexity**: quick-read
- **Priority**: medium — interesting agent workflow and a possible fit for video-production work, but short, light on detail, and the repo isn't named

**Why These Tags:**
The tool is an open-source project operated through AI coding agents (`ai`, `open-source`) whose output is video analysis and rebuild (`video-production`). `tutorial` and `actionable` because it walks through install, demo and a hands-on rebuild.

**Suggested Bases Filters:**
- Find similar content: `type = video AND tags contains "ai"`
- Find unwatched high-priority: `priority = high AND status = inbox AND read = false`

## 🔗 What to Explore Next

- rea-video GitHub repo and its demo cases
- Other agent-driven video analysis / video-to-code tools
- Remotion for programmatic video from web code
- Claude Code / Codex workflows for media tasks
- ITCoderGao's other agent tutorials (Hermes, Pi agent, ComfyUI)

---

**Captured**: 2026-11-20
**Source**: https://www.youtube.com/watch?v=Nlg7hKPPkSw
**Channel**: ITCoderGao

**Connection to Other Notes:**
- [[wiki/ai-tools/ai-tools|AI Tools]]
- [[wiki/ai-media/ai-media|AI Media]]
- [[wiki/claude-code/claude-code|Claude Code]]
