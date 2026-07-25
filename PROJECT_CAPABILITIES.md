# Agostino Scalzullo (Ostin Solo) — Project Capabilities Document

**Purpose:** Source of truth for Alignerr CV and applications. Not a resume.  
**Generated:** 2026-07-25  
**Sources:** M4 Pro laptop (`/Users/ostino`), Intel Mac via SSH (`Intel-mac` / `100.115.19.27`), Windows GPU host via SSH (`computerone` / `100.120.227.77`), GitHub `ostinsolo`, [vstopia.com](https://vstopia.com).

---

## 1. Profile snapshot

| Item | Detail |
|------|--------|
| Name | Agostino Scalzullo |
| Professional name | Ostin Solo |
| Location | London, United Kingdom (right to live and work in UK) |
| Contact | +44 7999 012772 · soloostin@aol.com |
| Sites | [ostinsolo.co.uk](https://ostinsolo.co.uk) · [vstopia.com](https://vstopia.com) · [github.com/ostinsolo](https://github.com/ostinsolo) · [LinkedIn](https://www.linkedin.com/in/agostino-scalzullo-156952121) |
| Languages | Italian (native); English (full professional, IELTS certified); Spanish (professional working) |
| Education | Music Production — SAE Institute (2019–2020); Electronic Music — Italian Conservatory; Liceo Scientifico; Spanish studies Valencia 2022 |

### Studio / listening chain (Alignerr-relevant)

- Beyerdynamic DT 990 Pro headphones
- Genelec M040 speakers
- Universal Audio Apollo Quad
- Lewitt LCT 640 microphone
- Dedicated listening environment

**Note:** Does **not** use Pro Tools day-to-day — skip Alignerr roles that require Pro Tools.

### Compute lab

| Machine | Spec / role |
|---------|-------------|
| **This laptop (M4 Pro)** | MacBook Pro, Apple M4 Pro, 14-core (10P+4E), **48 GB** — Metal / MPS / MLX development |
| **Intel-mac** | Ostins-MacBook-Pro.local, macOS 14.6.1, **x86_64** — large Max/JUCE/M4L/product archive + GPT-SoVITS |
| **computerone** | Windows GPU host — RTX class CUDA, Ollama, ComfyUI, FaceSwap, DSU Windows builds |
| Additional GPU | NVIDIA **RTX 3080 Ti** and **RTX 3070** in lab (cross-hardware eval) |
| **Hetzner** | VSTOPIA production (Docker, Traefik, Postgres, n8n, app.vstopia.com) |

---

## 2. Machine map (SSH inventory status)

| Alias | Host | User | Status (2026-07-25) |
|-------|------|------|---------------------|
| Intel-mac | 100.115.19.27 | ostinsolo | **Online** — inventory captured |
| computerone / gpu | 100.120.227.77 | 44746 | **Online** — inventory captured |
| win | 100.126.50.114 | soloo | Unreachable (port 22 fail) |

---

## 3. Owned products (commercial / shipping)

### 3.1 Doctor Sample Unit / Dynamic Split Module (DSU / DSm)

- **What:** Commercial Ableton Max for Live audio-separation and restoration environment; shared frozen runtime so end users need no Python.
- **Where:** `/Users/ostino/Desktop/main` (primary); Intel-mac `dsu`, `DSU(x86-mac)`; computerone `Desktop/WITHALL`, `DSU_VSTOPIA`.
- **Stack:** Python 3.10, PyTorch 2.x, **cx_Freeze**, Max for Live (`.amxd`), Node helpers; backends **CUDA / MPS / CPU**.
- **Models / workers:** Demucs (htdemucs/MDX), BS-RoFormer (28+ model variants), audio-separator, Apollo restoration, VR/MDX paths.
- **Capability signal:** Compared **60+** neural separation / restoration options for bleed, transients, phase, spectral artefacts, speed, hardware compatibility; regression fixtures for migrations.
- **CV keywords:** critical listening, model comparison, MPS/CUDA, frozen inference, product QA.

### 3.2 VSTOPIA

- **When:** **2023–Present**
- **What:** Curated marketplace / community for Max for Live and independent audio software; developers retain **90%** of sales; you host others’ products.
- **Live:** [vstopia.com](https://vstopia.com), app.vstopia.com.
- **Stack:** Laravel storefront + licensing (`LicensorA`), Node/Express + React/TS social-v2 (`HETNZER`), PostgreSQL, Docker Compose on **Hetzner**, Traefik, n8n; optional Ollama via Tailscale → computerone.
- **Capability signal:** Product standards, acceptance criteria, developer coordination, documentation curation, API/platform ops.
- **Note:** Prefer **Hetzner** on CV for VSTOPIA (Docker). **Heroku + MongoDB** are **AUDIOENCE production infra**, not VSTOPIA hosting. `Heroku-backup` on Intel-mac may still be related (historic/local backup), not primary VSTOPIA evidence.

### 3.3 Ostin Solo commercial Max / Ableton line

Portfolio evidence across machines and site:

| Product | Evidence |
|---------|----------|
| Dynamic Split / DSU | Desktop/main, DSm.amxd |
| YouTube 4 Live / YouTube4DAW | Intel-mac Code/Desktop; Desktop/main amxd |
| ASA Tin | Intel-mac ASA projects; computerone Desktop/ASA-Tin |
| Ableton Drive, ABL Series / bundles | Intel-mac |
| Preview Tuner, Clip Wizard, Pendolo, Device Window, Simpler+, Split Wizard+ | Prior CV + site portfolio; [Preview Tuner](https://ostinsolo.co.uk/devices/Preview-Tuner) — collaborated with Grammy-winning producer Connor McDonough on Preview Tuner (Max for Live tuning/preview workflow). Do **not** claim Connor collaborated on DSm/DSU (Gearnews cites him as an impressed user of DSm, not co-author). |
| Harmodulum | GitHub `Harmodulum` |
| Creator-Tool-VST | GitHub — screen+audio capture VST (C++) |
| DyERS | GitHub `DyERS-dynamic-resonance-suppressor` (JUCE spectral dyn EQ) — not on this laptop tree |

### 3.3b Industry press coverage (news / announcements)

Wording for CV: **covered in industry press** (not “reviewed by” unless a full review exists).

| Outlet | Product | URL |
|--------|---------|-----|
| Sound On Sound | Dynamic Split Module | https://www.soundonsound.com/news/vstopia-announce-dynamic-split-module-ableton |
| Gearnews | Dynamic Split Module | https://www.gearnews.de/elektron-tal-ni-ableton-sound-synth/ |
| Gearnews | Pendolo | https://www.gearnews.de/elektron-u-he-ni-moog-ableton-sounds/ |

### 3.4 AUDIOENCE

- **What:** Real-time remote collaboration plug-in (audio, MIDI, sync); product direction + coordinated VST3/AU work (WebRTC, Ableton Link).
- **Infrastructure:** Supporting API/platform on **Heroku + MongoDB** (production); keep WebRTC / Ableton Link in product framing.
- **Where:** Large trees on **Intel-mac** (`AUDIOENCE*`, plugin + API repos) and computerone `Documents/AUDIOENCE`.

---

## 4. Audio AI / inference optimisation

| Project | Path / repo | Role | Ownership |
|---------|-------------|------|-----------|
| DSU frozen runtimes | Desktop/main; cxfreeze builds | Ship Demucs/RoFormer/AudioSep without Python | **Owned** |
| audio-separator-cxfreeze | GitHub + Code | Frozen language-queried separation | **Owned packaging** |
| BS-RoFormer-freeze | GitHub + Intel-mac | Standalone BSS executable | **Owned packaging** |
| demucs-cxfreeze | GitHub + Intel-mac | Frozen Demucs + diffq | **Owned packaging** |
| spleeter-cxfreeze | GitHub + Code | macOS self-contained Spleeter (+ C RT paths) | **Owned packaging** |
| Roformer MLX C++ | `Code/Roformer_studies/roformer-mlx-cpp` | Python-free Metal inference; parity vs Python MLX | **Owned R&D** |
| GGUF/GGML RoFormer | Roformer_studies + BSRoformer.cpp | Convert/validate GGUF; CPU/CUDA/Vulkan refs | **Owned R&D** + upstream ref |
| Sample generator | Desktop/main + Code | FluCoMa / C++ stem → one-shots | **Owned** |
| Music-Source-Separation-Training | Intel-mac | Training reference / experiments | Study / mixed |

**Performance claim (for CV, keep honest — sourced):**

- **MLX vs prior MPS / `audio-separator` baselines (Apple Silicon):** up to **~1.85× median** faster local Python MLX inference across a validated 4-model overlap set; up to **~2.5×** on MelBand RoFormer and **~2.16×** on BS-RoFormer (M4 mini, MUSDB/ABBA subset). Source: `mlx-audio-separator/docs/release-validation.md` (and README caveats — not universal for all machines/models/inputs).
- **Native C++ MLX BS-RoFormer-SW (matched gate):** warm 6-stem separation of 10 s audio in **~3.6 s** → **RTF ≈ 0.36** (~**2.8× realtime**) on **M4 Pro**; C++ MLX path is **bit-exact** to Python MLX. Source: `roformer-mlx-cpp/docs/FIXED_BENCHMARK_GATE.md` (+ `artifacts/benchmark_fixed_10s/`).
- **Do not claim:** “**40% faster**” (no sourced 40% speedup; “40–45 s” was an internal time target). **Do not claim** C++ inference is faster than Python MLX — gate sets `performance_claim=false` / `python_removal_inference_claim=false` (warm inference delta < 5% policy). Optional honest note only: faster **model load/setup** (~412 ms → ~171 ms), not inference %.
- **sample-generator:** no verified speed/RTF benchmarks — do not invent speed claims.

**Python → C++:** Directed migration of performance-critical separation / inference components toward C++/MLX while preserving validated (bit-exact) reference behaviour; frame as parity + absolute RTF, not “C++ % faster than Python.”

---

## 5. Voice / STT / TTS / agents / MCP

| Project | Location | Notes |
|---------|----------|-------|
| MaxMSP Audio via UDP → STT | GitHub `MaxMSP-Audio-via-UDP-for-voice-recognition` | Float32 transport, buffering, Vosk path |
| Moonshine | Code/moonshine; computerone Documents/CODE | On-device STT/TTS toolkit (upstream + local use) |
| Local voice / tool orchestration | Prior CV + Leonardo / FunctionGemma / Moonshine work | Ableton + tool-calling assistant (WIP) |
| GPT-SoVITS / OpenVoice / RVC | Intel-mac Documents | Voice clone / TTS experimentation |
| Qwen3-TTS | Code/QWEN3-TTS; computerone Desktop | Local TTS |
| Leonardo II agent-sandbox | Code/Leonardo II | Docker agents, Guardian, **Ollama only**, MCP optional |
| Leonardo-Y / JARVIS | GitHub; computerone `.jarvis` | Personal assistant experiments |
| MaxMSP-MCP-Server | `src/external` | **Upstream** MCP for Max patch LLM tools |
| Ollama | computerone `.ollama`; Hetzner proxy path | GPU inference for product tooling |

---

## 6. Platform / APIs / private AI media

| System | Stack | CV framing |
|--------|-------|------------|
| VSTOPIA store + licensing | Laravel, Electron protector-builder, API | Product + licensing platform |
| AUDIOENCE API | Heroku, MongoDB | Realtime collaboration backend (with WebRTC / Ableton Link client) |
| social-v2 (HETNZER) | Node, React, Postgres, Docker, Hetzner | Creator OS / ops |
| Private GPU AI path | Tailscale → computerone Ollama / ComfyUI | Local LLM + image pipelines for product tooling |
| ComfyUI + FaceSwap + Influencer-Generator | computerone | Private image/video AI generation platform |
| StyleGAN2/3, LoRA training | computerone | Model training / generation experiments |
| N8N / N8N4VPS | Intel-mac + computerone + Hetzner | Automation (keep CV-light; avoid scrape framing) |

**Do not lead with** Instagram engagement orchestration / unofficial scraping (InstaGPy) on Alignerr applications.

---

## 7. Vision / CV / AR (OpenCV · MediaPipe · Depth · MoGe · face)

Deep search (2026-07-25) across M4 laptop, Intel-mac, and computerone. You have a **full multimodal stack**: computer vision + generative face/image + audio ML + Max/JUCE productization.

### 7.1 Owned / integrated vision systems (M4 Pro)

| Project | Path | Stack | What you can do |
|---------|------|-------|-----------------|
| **Depth-Anything-V2 + Max package** | `Documents/Code/Depth-Anything-V2` | Depth Anything V2, **MoGe-2** (Microsoft MoGe), OpenCV, Core ML/ANE, AprilTag, Max/Jitter C++ (`jit.depthanything`, `jit.moge2`, projection mask) | Real-time monocular depth, metric geometry (MoGe-2), camera→projector UV warp, tag tracking in Ableton/Max |
| **Yolo11 sign → synth** | `Documents/Code/Yolo11-sign-lanugage-detection` | **YOLOv11**, **MediaPipe**, **OpenCV**, **ONNX**, Node/React, Web Audio | Custom-trained hand-sign detection (46 classes) → musical controls |
| **MAKE-UP APP** | `Documents/Code/MAKE-UP APP` | iOS ARKit/Vision/Metal, **MediaPipe** face/hand landmarker research, CoreML Face Parsing, Banuba refs | Real-time makeup coaching / face tracking / stencil scoring (not a filter app) |
| **Projector_studies** | `Documents/Code/Projector_studies` | OpenCV, ChArUco, GS-ProCams research | ProCam calibration; flat-wall MVP validated |
| **splash** | `Documents/Code/splash` | Multi-projector mapping, OpenCV | Video mapping / depthmap-related mapping |
| **Deep-Live-Cam** | `Documents/Code/Deep-Live-Cam` | OpenCV, ONNX, InsightFace, CoreML path | Real-time face swap (upstream + local GPU runs) |
| **LiveAvatar** | `Documents/Code/LiveAvatar` | OpenCV, ONNX, Whisper, InsightFace, diffusion | Audio-driven talking avatar |
| **DMX-4-CD** | `Documents/Code/DMX-4-CD*` | Max Jitter, Art-Net | Lighting + 3D scene control |

### 7.2 Intel-mac vision / CV bridges

| Project | Notes |
|---------|-------|
| **Whisper_wrapper** (`~/Whisper_wrapper*`) | OpenCV via `cv.jit` / OpenCVsupport; Whisper / faster-whisper; **denoiser~ / Demucs ONNX** Max externals — audio+vision Max bridge |
| Max `rtpsendreceive` / vcpkg | OpenCV / OpenCV3 ports for Max RTP |
| Three.js template | `@mediapipe` dependency (lighter) |
| Max Package **denoiser** under Chords Voice Generator | **Facebook Denoiser** in Max for Live context |
| **sherpa-onnx**, ONNX model packs | ASR / embedding ONNX deployment |

### 7.3 computerone — generative vision / face platform

| Project | Capability |
|---------|------------|
| **ComfyUI** (+ workflows) | Node-graph image/video generation |
| **FaceSwap*** (many pipelines) | Production face-swap / influencer media |
| **DeepFaceLab**, **VisoMaster**, **InsightFace** | Face identity / swap training tooling |
| **Influencer-Generator** | App + Comfy workflows |
| **StyleGAN2/3**, **sd-scripts**, LoRA training | GAN + Stable Diffusion fine-tuning |
| **ai-toolkit**, `models/zit_diffusers` | Diffusion checkpoints / training |

### 7.4 Keyword → where it lives

| Keyword | Strongest homes |
|---------|-----------------|
| **OpenCV** | Depth-Anything Max package, Yolo11, Projector_studies, Deep-Live-Cam, LiveAvatar, splash, Whisper_wrapper (Intel), DeepFaceLab (Win) |
| **MediaPipe** | Yolo11 (pip), MAKE-UP APP (headers/research) |
| **Depth Anything** | `Depth-Anything-V2` + Max ANE path (M4); transformers venvs elsewhere |
| **MoGe-2** | Vendored/integrated under `Depth-Anything-V2/max_external` (not a standalone clone) |
| **Denoiser** | Custom envelope denoise in DSU `noise_reduction`; Facebook Denoiser Max package on Intel-mac; AFTER internal diffusion “Denoiser” class (different) |
| **Facebook Research lineage** | **Demucs** (facebookresearch) via DSU / demucs-cxfreeze / Roformer MLX demucs ports; Facebook Denoiser Max; not a general “Facebook clone farm” |
| **ONNX** | Yolo11, Deep-Live-Cam, LiveAvatar, moonshine, sherpa-onnx, Demucs ONNX in Whisper_wrapper, Roformer convert extras |
| **Core ML / ANE** | Depth-Anything Max Small on ANE; MAKE-UP Face Parsing; Deep-Live-Cam Darwin notes |
| **YOLO** | Yolo11-sign-language-detection (custom trained) |
| **Whisper / STT** | moonshine, Whisper_wrapper, LiveAvatar, ACE-Step helpers, JARVIS (Win) |
| **RVC / SoVITS / voice** | Intel-mac GPT-SoVITS, RVC1006, OpenVoice; Win XTTC/XTTS-RVC; Max RVC_pro_multi |

---

## 7b. Expanded “what you can do” (skill clusters)

Use this when explaining capabilities to Alignerr / clients:

1. **Critical audio QA + stem separation productization** — DSU/DSm, 60+ models, cx_Freeze, MPS/CUDA/Intel Mac.
2. **Native inference optimisation** — Roformer MLX C++ / GGUF/GGML; up to ~1.85× median MLX vs MPS/audio-separator (≤~2.5× MelBand); RTF ≈ 0.36 on M4 Pro 6-stem BS-RoFormer (do not claim 40% or C++>Python inference).
3. **Voice AI** — STT/TTS/clone (Moonshine, Whisper wrappers, GPT-SoVITS, RVC, Qwen3-TTS, OpenVoice).
4. **Computer vision in Max / Ableton** — Depth Anything + MoGe-2 + AprilTag + OpenCV projection.
5. **Hand/face interactive systems** — MediaPipe + YOLOv11 sign→music; iOS AR makeup coaching.
6. **Generative image/video pipelines** — ComfyUI, FaceSwap, StyleGAN, LoRA on Windows GPU.
7. **Realtime collaboration audio** — AUDIOENCE (JUCE/WebRTC/Ableton Link).
8. **Platform engineering** — VSTOPIA marketplace + Hetzner Docker + APIs + licensing.
9. **Local agents / MCP** — Leonardo sandbox, Ollama GPU over Tailscale, Max MCP tools.
10. **Creative hardware** — DMX/Art-Net, sensors, projection mapping.

---

## 8. Study / upstream clones (mark clearly)

Hands-on evaluation / integration only unless you shipped changes:

- AFTER (diffusion → Max/nn_tilde) — internal Denoiser ≠ facebookresearch/denoiser
- ACE-Step-1.5
- Deep-Live-Cam, LiveAvatar (heavy local use / private platform adjacent)
- splash (Splashmapper)
- MaxMSP-MCP-Server, kalibr, vst3_public_sdk
- moonshine upstream tree
- Depth Anything / MoGe upstream papers with **your** Max external packaging on top

---

## 9. Exclude from Alignerr CV

- Crypto / Pump.fun trading bots; `token-creator-monitor`
- Social engagement scraping / unofficial Instagram API framing
- Long nightlife venue storytelling (keep 1–2 bullets max)
- Claiming **professional voice actor** without paid VO credits
- Claiming **Data Science Expert** (role wants DS Master’s/PhD)
- Do not present Heroku as VSTOPIA hosting; do mention Heroku + MongoDB for AUDIOENCE

---

## 10. Alignerr role mapping

| Role | Fit | Supporting evidence |
|------|-----|---------------------|
| **Audio Quality Reviewer** | **Strong — apply first** | Critical listening, DSU model eval, STT/transcript work, DT 990 Pro + Genelec M040 + Apollo + Lewitt LCT 640 |
| **AI Trainer Specialist** | **Apply** | Rubrics, batch evaluation, multi-format (audio/image/text) QA |
| **Software Engineer Task Author (London/UK)** | **Strong** | C++/Python/Max/JUCE, frozen runtimes, Docker/Hetzner, agent sandboxes, debugging systems |
| Audio Engineer – Pro Tools | **Skip** | Does not use Pro Tools day-to-day; do not claim PT for Alignerr |
| Product Review Analyst | Weak / optional | VSTOPIA product QA stretch only |
| Professional Voice Actor – Italian | **Only if paid VO + LDM** | Native Italian + studio ≠ VO career |
| Data Science Expert | **Skip** | Credential mismatch |

### Preferred CV title line

`AI AUDIO EVALUATOR | AUDIO QUALITY REVIEWER | AI SYSTEMS SPECIALIST`

---

## 11. Core skills (evidence-backed, for CV Core Expertise)

**Audio quality evaluation:** critical listening; clarity/intelligibility; noise; clipping; distortion; pronunciation; unnatural phrasing; frequency imbalance; phase; transients; source bleed; spectral artefacts; A/B comparison; structured rubrics; actionable feedback.

**Speech & transcription:** audio-to-transcript verification; STT validation; accents; contextual errors; unclear segments; Moonshine/Vosk/UDP Max pipelines.

**Audio engineering & music tech:** Ableton Live; Max/MSP / Max for Live; signal flow; EQ; noise reduction; mixing/mastering (SAE); neural source separation; real-time audio; WebRTC/Ableton Link (AUDIOENCE).

**AI evaluation & software systems:** model comparison; acceptance criteria; regression testing; function calling / agents; local models (Ollama, MLX, GGUF); C++; Python; JavaScript/Node; JUCE; cx_Freeze; Docker; APIs; Heroku; MongoDB; cross-platform macOS (Intel + Apple Silicon) / Windows CUDA validation.

**Computer vision & multimodal:** OpenCV; MediaPipe; YOLOv11/ONNX; Depth Anything V2; MoGe-2; AprilTag; Core ML/ANE; InsightFace / face-swap pipelines; ComfyUI; Max/Jitter vision externals; projector–camera calibration.

---

## 12. Appendix A — GitHub `ostinsolo` (public)

ableton-js · Audio-Engineer-Sound-Design-LLM · audio-separator-cxfreeze · BS-RoFormer-freeze · Creator-Tool-VST · DDSP-M4L · demucs-cxfreeze · DyERS-dynamic-resonance-suppressor · everything-claude-code · Harmodulum · kalibr · Leonardo-Y · maxdevtools · MaxMSP-Audio-via-UDP-for-voice-recognition · Ollama-SwiftUI · Projector_studies · reachy_mini_conversation_app · rotary-encoder-over-mcp23017 · spleeter-cxfreeze · Three.js-Training-Template · vst3_public_sdk

---

## 13. Appendix B — M4 Pro `Documents/Code` (high level)

ACE-Step-1.5 · AFTER · AI for gen~ · AudioSep-cxfreeze · CEF_MFL_BACKUP · DMX-4-CD · DSU(arm64-mac) · Deep-Live-Cam · Depth-Anything-V2 · HETNZER · Leonardo II · LiveAvatar · MAKE-UP APP · Novation_debug · Projector_studies · QWEN3-TTS · Resume · Roformer_studies · Study for Cyber Security · Yolo11-sign-lanugage-detection · glaston board · moonshine · sample-generator · splash · spleeter-cxfreeze

Plus: `Desktop/main` (DSU), `Developer/vst3sdk`, `src/external/{MaxMSP-MCP-Server, py-js}`

---

## 14. Appendix C — Intel-mac highlights

- Huge **AUDIOENCE** product/API/packaging tree
- **YouTube4DAW / YouTube 4 Live**, ASA Tin, Ableton Drive, JUCE projects
- **GPT-SoVITS**, OpenVoice, RVC, TTS stacks
- demucs/BS-RoFormer/SpleeterRT freestanding builds
- VSTOPIA prod / public_html / LicensorA
- N8N, Heroku-backup (legacy)

---

## 15. Appendix D — computerone (Windows GPU) highlights

- ComfyUI, FaceSwap family, Influencer-Generator, StyleGAN, LoRA training
- Ollama, JARVIS, qwen3-TTS, DeepFaceLab
- WITHALL / DSU Windows orchestration, ASA-Tin, LicensorA, N8N4VPS
- Ableton + Max 8/9 + Visual Studio toolchains

---

## 16. Draft CV “Additional / remote setup” line

> Equipped for remote audio-evaluation work with Beyerdynamic DT 990 Pro headphones, Genelec M040 speakers, Universal Audio Apollo Quad, Lewitt LCT 640 microphone, and a dedicated listening environment; NVIDIA RTX 3080 Ti / 3070 and Apple M4 Pro (48 GB) plus Intel Mac systems for Metal, MPS, MLX and GGUF local-model evaluation. Based in London with the right to live and work in the United Kingdom.

---

## 17. Appendix E — Deep search captures (2026-07-25)

Local tool dumps (this machine):

- `/tmp/local-vision-audio-projects.md` — M4 OpenCV/MediaPipe/Depth/MoGe inventory  
- `/tmp/deep-projects-summary.md` — Intel-mac + computerone unique folders  
- `/tmp/intel-mac-deep-projects.txt` — raw Intel-mac find  
- `/tmp/computerone-deep-projects-full.txt` — raw Windows find  

**Facebook / Demucs note:** Primary Facebook Research lineage in your work is **Demucs** (and Max Facebook Denoiser package on Intel-mac), productized inside DSU — not a separate “Facebook projects” folder.

*End of capability document. Distill selectively into Alignerr CV; do not paste this whole file into applications.*
