# Awesome AI Video Models [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> The most complete, up-to-date comparison of AI video generation models — **which model, via which API, at what price, and how fast.**

Unlike other lists that just dump links, this one answers the question developers actually have: *"I need to generate video — which model do I pick, and where do I call it?"* Every model below is mapped to the APIs that serve it, with indicative pricing, speed, and max resolution/duration.

> 💡 Prices are per **second of output video** (retail API rates verified July 2026) and move fast — always confirm against the provider. Latency is a rough "time to first result" at default settings.

<p align="center">
  <a href="https://www.youtube.com/watch?v=SOXsxqnQGlc">
    <img src="docs/assets/video-36-thumbnail.png" alt="Best AI Video Generator (API) in 2026 (Quality, Price, Uncensored, Editing)" width="640">
  </a>
</p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=SOXsxqnQGlc"><b>📺 Best AI Video Generator (API) in 2026 (Quality, Price, Uncensored, Editing) →</b></a>
</p>

## Related Projects

- [awesome-uncensored-ai-video-models](https://github.com/Anil-matcha/awesome-uncensored-ai-video-models) — Filtering-, access-, and licensing-focused companion catalog for local and hosted video model variants
- [MuAPI video-generation docs](https://muapi.ai/docs/video-generation) — Use the models compared here through one unified API.
- [MuAPI model playground](https://muapi.ai/playground) — Test video models before choosing an integration.
- [MiniMax-H3-API](https://github.com/Anil-matcha/MiniMax-H3-API) — Python SDK for MiniMax H3 text-to-video, image-to-video, and first/last-frame video generation.
- [awesome-minimax-h3-prompts](https://github.com/Anil-matcha/awesome-minimax-h3-prompts) — Prompt gallery with runnable MiniMax H3 video examples.
- [Wan-3.0-API](https://github.com/Anil-matcha/Wan-3.0-API) — Python SDK and MCP server for Wan 3.0-compatible video generation.
- [Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI) — curated hub of open generative-media tools and pipelines
- [Text-To-Video-AI](https://github.com/SamurAIGPT/Text-To-Video-AI) — generate a finished video from a text prompt end-to-end
- [Open-AI-Micro-Drama-Generator](https://github.com/Anil-matcha/Open-AI-Micro-Drama-Generator) — multi-scene AI micro-drama pipeline
- [Veo-4-API](https://github.com/Anil-matcha/Veo-4-API) — Python wrapper for Google Veo 4
- [Seedance-2-API](https://github.com/Anil-matcha/Seedance-2-API) — Python wrapper for ByteDance Seedance 2
- [awesome-seedance-2.5-api-prompts](https://github.com/Anil-matcha/awesome-seedance-2.5-api-prompts) — prompt library for Seedance 2.5
- [ai-creator-academy](https://github.com/Anil-matcha/ai-creator-academy) — free curriculum teaching creators how to monetize the models compared in this list
- [Flux-3-Dev-API](https://github.com/Anil-matcha/Flux-3-Dev-API) — Python wrapper for Black Forest Labs' FLUX 3 (Dev variant) — text-to-image, image-to-image, text-to-video, image-to-video
- [awesome-flux-3-api-prompts](https://github.com/Anil-matcha/awesome-flux-3-api-prompts) — FLUX 3 API guide, prompts, and parameters
- [wan-3.0-comfyui](https://github.com/Anil-matcha/wan-3.0-comfyui) — ComfyUI custom nodes for Wan 3.0 text-to-image, image edit, text-to-video, and image-to-video via MuAPI.
- [Video-Utilities-API](https://github.com/Anil-matcha/Video-Utilities-API) — compare Muapi video upscaling and video-to-audio post-production endpoints.

## Contents

- [Commercial models (closed, API-only)](#commercial-models-closed-api-only)
- [Open-source models (self-host or API)](#open-source-models-self-host-or-api)
- [Task-specific: image-to-video](#task-specific-image-to-video)
- [Avatar & talking-head models](#avatar--talking-head-models)
- [Real-time & interactive video](#real-time--interactive-video)
- [Video upscaling & enhancement](#video-upscaling--enhancement)
- [Benchmarks & leaderboards](#benchmarks--leaderboards)
- [How to choose](#how-to-choose)
- [Where to run them (API providers)](#where-to-run-them-api-providers)
- [Contributing](#contributing)

## Commercial models (closed, API-only)

| Model | Maker | Best for | APIs | Price / sec | Max res / length | Notes |
|-------|-------|----------|------|-------------|------------------|-------|
| **Seedance 2.5** | ByteDance | 🏆 Best overall quality | Fal, Replicate, MuAPI | ~$0.05–0.25 by resolution | 4K / up to 30s, 50 refs | Multimodal references, multi-scene continuity, audio-video in one pass; also ships dedicated **Video Edit** and **Spicy** (uncensored) endpoints |
| **Veo 3.1** | Google | Realism + native audio | Gemini API, Fal, Replicate, MuAPI | $0.15 Fast · $0.40 Quality (Lite $0.03–0.05) | 1080p/4K / ~8s | Independent editorial consensus "leads the field" on scene consistency/prompt understanding |
| **Sora 2** | OpenAI | Coherence, long shots | OpenAI API | $0.10 Std · $0.30–0.50 Pro | 720p–1080p / ≤25s | ⚠️ API sunsets **Sept 24, 2026** — don't build against it near/after that date |
| **Kling v3.0** | Kuaishou | Motion, prompt adherence | Fal, Replicate, MuAPI | ~$0.10 (up to $0.20 w/ audio); ~$0.075 via resellers | 1080p / 5–10s | **Omni** variant (reference-driven multi-image editing/generation) and dedicated **Pro Motion Control** endpoint ($0.16/sec, complex cinematic camera work) available |
| **Runway Gen-4.5 / Aleph** | Runway | 🏆 Best video-to-video editing (outside benchmark) | Runway API, Fal, MuAPI | $0.12 (Turbo $0.05) | 1080p / ~10s | Aleph is the model most cited as the outside comparison point in editing benchmarks; **Act-Two** ($0.07/generation) does performance transfer (facial/motion) onto a static character instead |
| **Seedance 2.0** | ByteDance | 🏆 Best value at scale | Fal, Replicate, MuAPI | ~$0.025 Mini · ~$0.05 Pro | 1080p / 5–10s | Cheapest production-grade video API in independent pricing research |
| **PixVerse V6** | PixVerse | Flexible low-cost tiers | Fal, MuAPI | $0.033 (360p, no audio) – $0.150 (1080p, w/ audio) | 1080p / ~5–8s | Price genuinely scales with resolution, unlike flat per-generation competitors |
| **Vidu Q3 Pro** | ShengShu/Vidu | Cheap high-quality generation | MuAPI | ~$0.04/generation | 1080p | Independently ranks #2 on outside quality lists |
| **Gemini Omni Video Edit** | Google | 🏆 Best any-to-any editing | Gemini API, MuAPI | Flat $2.40 (720p/1080p) / $3.60 (4K) | 4K | Natively multimodal — rewrites visuals + audio jointly in one pass; not available on Fal, a real MuAPI differentiator |
| **Hailuo 2.3 / MiniMax H3** | MiniMax | Character motion; H3 Open ships open-weights | Fal, Replicate, MuAPI | $0.045 (768p) · ~$0.017 (512p) | 1080p / ≤10s | 30–90s generation; H3 Open variant is open-weights, listed separately below |
| **Luma Ray 3** | Luma | Fast iteration, HDR | Luma API, Fal | ~$0.21 (HDR ~2×) | 1080p+HDR / 5–10s | Per-second billing |
| **Pika 2.2** | Pika | Effects, stylization | Pika API | ~$0.05 | 1080p / ~5s | Cheapest closed model |
| **Wan 2.6 / 3.0** | Alibaba | Cheapest native 1080p (2.6); next-gen (3.0) | MuAPI | $0.05/sec (2.6) | 1080p | Both API-only (not open-weight, unlike Wan 2.2 below); **Wan 3.0 not live yet** as of Aug 2026 |

## Open-source models (self-host or API)

| Model | Maker | License | Best for | APIs | Self-host VRAM |
|-------|-------|---------|----------|------|----------------|
| **Wan 2.2** | Alibaba | Apache-2.0 | Quality leader; T2V+I2V+edit in one | Fal, Replicate | ~24GB+ |
| **MiniMax H3 Open** | MiniMax | Open weights | Native stereo audio, general open-source video gen | Fal, MuAPI | ~24GB+ |
| **HunyuanVideo 1.5** | Tencent | Custom OSS | Natural motion & physics | Fal, Replicate | ~40GB+ |
| **LTX-2.5** | Lightricks | OpenRAIL | Fast; native 4K + synced audio (latest release, supersedes 2.3) | Fal, MuAPI | ~12GB+ |
| **CogVideoX** | Zhipu / THUDM | Apache-2.0 | Research, fine-tuning | self-host | ~18GB+ |
| **Mochi 1** | Genmo | Apache-2.0 | High-fidelity motion | Fal, self-host | ~24GB+ |
| **Open-Sora 2.0** | HPC-AI Tech | Apache-2.0 | Fully open pipeline + weights | self-host | ~24GB+ |
| **SkyReels-V3** | Skywork | Custom OSS | Cinematic / film-style shots | self-host | ~24GB+ |
| **NVIDIA Cosmos** | NVIDIA | NVIDIA OpenModel | World models, robotics/sim | self-host | ~40GB+ |
| **AnimateDiff** | Community | Apache-2.0 | Add motion to SD image models | self-host | ~10GB+ |

## Task-specific: image-to-video

Most models above also do image-to-video (I2V). Strongest I2V specifically:

- **Kling 3.0** — best all-round I2V motion
- **Seedance 2.0** — best price/quality for I2V
- **Wan 2.2** — best open-source I2V
- **Luma Ray 3** — fastest I2V for iteration

## Avatar & talking-head models

Portrait/presenter video from a photo or actor + script. These bill by subscription or per-minute credits (not per-second like the raw generators), so the pricing column names the *model*, not a rate.

| Tool | Maker | Best for | API | Pricing model |
|------|-------|----------|-----|---------------|
| **HeyGen** | HeyGen | Studio avatars, dubbing | Yes (+ streaming SDK) | Credits / subscription |
| **Synthesia** | Synthesia | Enterprise training videos | Yes | Seat / subscription |
| **D-ID** | D-ID | Real-time talking portraits | Yes (streaming) | Per-minute credits |
| **Hedra** | Hedra | Expressive character audio→video | Yes | Credits |
| **Tavus** | Tavus | Conversational video agents | Yes | Per-minute |
| **Captions (Mirage)** | Captions | Fully generated AI actors | Yes | Credits / subscription |
| **Hour One** | Hour One | Scalable presenter video | Yes | Subscription |

Open-source alternatives: **OmniHuman-1**, **LivePortrait**, **EchoMimicV2**, **MuseTalk**, **OmniAvatar** (self-host, see repos).

## Real-time & interactive video

Emerging category — sub-second/streaming generation for games, live avatars, and interactive worlds.

- **Decart (Lucy)** — real-time world/video generation
- **Krea Realtime 14B** — open-weights real-time generation
- **LongLive** — long-duration real-time generation
- **PixVerse** — fast interactive generation
- **Hunyuan-GameCraft / world models** — playable generated environments

## Video upscaling & enhancement

Post-process generated (or real) footage — upscale, interpolate, denoise.

| Tool | Type | Best for |
|------|------|----------|
| **Topaz Video AI** | Commercial | Highest-quality upscale + interpolation |
| **FlashVSR** | Open source | Fast video super-resolution |
| **Video2X** | Open source | Free upscaling (waifu2x/Real-ESRGAN) |
| **REAL Video Enhancer** | Open source | Interpolation + upscaling GUI |

## Benchmarks & leaderboards

Don't trust a maker's own demo reel — check independent evals before committing:

- **[VBench / VBench-2.0](https://github.com/Vchitect/VBench)** — 16-dimension automated quality benchmark
- **Artificial Analysis Video Arena** — Elo-style human-preference leaderboard across commercial + open models
- **Video-Bench** — human-aligned evaluation suite

## How to choose

- **Best overall quality** → Seedance 2.5, or Veo 3.1 for scene consistency/prompt understanding (Sora 2 works too, but its API sunsets Sept 2026)
- **Best value at scale** → Seedance 2.0 Mini (~$0.025/s) or PixVerse V6 (from $0.033/s, scales with resolution)
- **Best uncensored / unrestricted** → Seedance 2.5 Spicy, MiniMax H3 Open, or LTX-2.5
- **Best editing (video-to-video)** → Gemini Omni Video Edit (any-to-any, visuals+audio jointly) or Runway Aleph (most-cited outside benchmark)
- **Best motion/camera control** → Kling v3.0 Pro Motion Control (dedicated endpoint) or Runway Act-Two / Wan2.2 Animate (performance transfer)
- **Fully open / self-hosted** → Wan 2.2 (quality), MiniMax H3 Open, or LTX-2.5 (speed)

## Where to run them (API providers)

Aggregators that expose many of the above behind one API/key:

- **[MuAPI](https://muapi.ai)** — unified API across image + video models (Kling, Veo, Seedance, Hailuo, Wan, and more), one key, one billing
- **[Fal](https://fal.ai)** — fast inference, broad model catalog
- **[Replicate](https://replicate.com)** — pay-per-run, large community model catalog

Native APIs (single-vendor): Google Gemini (Veo), OpenAI (Sora), Runway, Luma, Pika, MiniMax.

## Contributing

PRs welcome. When adding a model, keep the table columns filled — **a row without provider + price + speed isn't useful.** New models go in the correct table (commercial vs open-source) and stay sorted by relevance.

---

*Maintained alongside [Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI). Found it useful? ⭐ the repo.*
