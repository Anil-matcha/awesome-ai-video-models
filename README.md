# Awesome AI Video Models [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> The most complete, up-to-date comparison of AI video generation models — **which model, via which API, at what price, and how fast.**

Unlike other lists that just dump links, this one answers the question developers actually have: *"I need to generate video — which model do I pick, and where do I call it?"* Every model below is mapped to the APIs that serve it, with indicative pricing, speed, and max resolution/duration.

> 💡 Prices are per **second of output video** (retail API rates verified July 2026) and move fast — always confirm against the provider. Latency is a rough "time to first result" at default settings.

## Related Projects

- [Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI) — curated hub of open generative-media tools and pipelines
- [Text-To-Video-AI](https://github.com/SamurAIGPT/Text-To-Video-AI) — generate a finished video from a text prompt end-to-end
- [Open-AI-Micro-Drama-Generator](https://github.com/Anil-matcha/Open-AI-Micro-Drama-Generator) — multi-scene AI micro-drama pipeline
- [Veo-4-API](https://github.com/Anil-matcha/Veo-4-API) — Python wrapper for Google Veo 4
- [Seedance-2-API](https://github.com/Anil-matcha/Seedance-2-API) — Python wrapper for ByteDance Seedance 2
- [awesome-seedance-2.5-api-prompts](https://github.com/Anil-matcha/awesome-seedance-2.5-api-prompts) — prompt library for Seedance 2.5
- [ai-creator-academy](https://github.com/Anil-matcha/ai-creator-academy) — free curriculum teaching creators how to monetize the models compared in this list
- [Flux-3-Dev-API](https://github.com/Anil-matcha/Flux-3-Dev-API) — Python wrapper for Black Forest Labs' FLUX 3 (Dev variant) — text-to-image, image-to-image, text-to-video, image-to-video
- [awesome-flux-3-api-prompts](https://github.com/Anil-matcha/awesome-flux-3-api-prompts) — FLUX 3 API guide, prompts, and parameters

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
| **Veo 3.1** | Google | Realism + native audio | Gemini API, Fal, Replicate, MuAPI | $0.15 Fast · $0.40 Quality (Lite $0.03–0.05) | 1080p/4K / ~8s | Native audio; 4K at premium |
| **Sora 2** | OpenAI | Coherence, long shots | OpenAI API | $0.10 Std · $0.30–0.50 Pro | 720p–1080p / ≤25s | ⚠️ API sunsets **Sept 24, 2026** |
| **Kling 3.0** | Kuaishou | Motion, prompt adherence | Fal, Replicate, MuAPI | ~$0.10 (up to $0.20 w/ audio); ~$0.075 via resellers | 1080p / 5–10s | Motion Control variant available |
| **Runway Gen-4.5** | Runway | Creative control, editing | Runway API, Fal | $0.12 (Turbo $0.05) | 1080p / ~10s | Strong editing suite |
| **Seedance 2.0** | ByteDance | Value, speed, quality | Fal, Replicate, MuAPI | ~$0.03 Fast · ~$0.05 Pro | 1080p / 5–10s | 2.5 in beta: 30s clips, 50 refs, pricing TBA |
| **Hailuo 2.3** | MiniMax | Character motion | Fal, Replicate, MuAPI | $0.045 (768p) · ~$0.017 (512p) | 1080p / ≤10s | 30–90s generation |
| **Luma Ray 3** | Luma | Fast iteration, HDR | Luma API, Fal | ~$0.21 (HDR ~2×) | 1080p+HDR / 5–10s | Per-second billing |
| **Pika 2.2** | Pika | Effects, stylization | Pika API | ~$0.05 | 1080p / ~5s | Cheapest closed model |

## Open-source models (self-host or API)

| Model | Maker | License | Best for | APIs | Self-host VRAM |
|-------|-------|---------|----------|------|----------------|
| **Wan 2.2** | Alibaba | Apache-2.0 | Quality leader; T2V+I2V+edit in one | Fal, Replicate | ~24GB+ |
| **HunyuanVideo 1.5** | Tencent | Custom OSS | Natural motion & physics | Fal, Replicate | ~40GB+ |
| **LTX-2.3** | Lightricks | OpenRAIL | Fast; native 4K + synced audio | Fal | ~12GB+ |
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

- **Best realism / audio** → Veo 3.1 (Sora 2 works too, but its API sunsets Sept 2026)
- **Best value at scale** → Seedance 2.0 (~$0.03/s) or Pika 2.2 (~$0.05/s)
- **Fastest iteration** → Luma Ray 3 or LTX-2.3
- **Fully open / self-hosted** → Wan 2.2 (quality) or LTX-2.3 (speed)
- **Editing & creative control** → Runway Gen-4.5

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
