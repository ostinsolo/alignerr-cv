# Agostino Scalzullo
**Audio Software & Creative Technology Engineer**
C++ · DSP · JUCE · Max/MSP · Audio ML · Deep Learning · Real-Time Systems · Computer Vision

London, UK · OSTIN SOLO · Founder, VSTOPIA
contact@ostinsolo.co.uk · [Live Portfolio](https://ostinsolo.github.io/ostin-solo-portfolio/) · [GitHub](https://github.com/ostinsolo)

## Index
[Profile](#profile) · [Core Skills](#core-skills) · [Selected Work](#selected-work) · [Engineering Validation](#engineering-validation) · [Experience](#experience) · [Education](#education) · [Languages](#languages) · [Recognition](#recognition--public-evidence)

## Profile
Audio software and creative-technology engineer working across native C++, DSP, plug-ins, neural audio, computer vision, networked audio and interactive hardware. Founder of VSTOPIA and developer of commercial OSTIN SOLO music-production software, with experience taking experimental systems through native implementation, testing, deployment, licensing and distribution.

## Core Skills
**Native audio:** C/C++, Objective-C++, JUCE, Max SDK, VST3/AU, DSP, MIDI/MPE
**ML / deep learning / vision:** source separation, BS-RoFormer, Demucs, MossFormer2, ECAPA speaker embeddings, target-speaker extraction, MLX, Core ML, CLAP embeddings, Depth Anything, MediaPipe, ARKit
**Realtime / platform:** WebRTC, Opus, RTP MIDI, WebSockets, AVFoundation, hardware APIs, Swift/SwiftUI, macOS/iOS
**Engineering:** profiling, benchmark design, parity/regression testing, model/runtime packaging, Developer ID signing and notarization
**Cross-platform builds:** macOS Apple Silicon & Intel, Windows x64/ARM64, cross-architecture toolchains, conditional compilation and release packaging

## Selected Work
### DSm — Dynamic Split Module
Neural separation, restoration and web-sampling environment for Ableton Live, created by combining and extending the earlier Split Wizard+ and YouTube 4 Live projects, with 63 model workflows spanning Demucs, RoFormer and related architectures. Covered by Sound On Sound and listed in the official Cycling ’74 project ecosystem.
[Product](https://vstopia.com/max-for-live-devices/dynamic-split-module) · [Sound On Sound](https://www.soundonsound.com/news/vstopia-announce-dynamic-split-module-ableton) · [Cycling ’74](https://cycling74.com/projects/dynamic-split-module-websampler-with-63-audio-separation-models-in-ableton-1)

### Native RoFormer External & VST3/AU — Work in Progress
Native C++/MLX implementation bringing six-stem BS-RoFormer separation into a Max/MSP external and an in-development plug-in architecture. Across tested Apple Silicon workloads, optimisation achieved a **median 1.85× speedup**, reaching **2.5× on MelBand RoFormer**; native six-stem BS-RoFormer achieved **RTF ≈ 0.36 (~2.8× real time)** on M4 Pro with bit-exact parity against the Python MLX reference.

### AUDIOENCE
JUCE/C++ networked collaboration plug-in architecture combining real-time audio, MIDI, WebRTC/P2P communication, Opus/PCM modes, resampling and DAW synchronisation across macOS and Windows.
[Official project](https://vstopia.com/audioence) · [Technical manual](https://vstopia.com/audioence-manual)

### Native Max / MPE / Hardware Systems
Native C++ Max externals for multitouch, MPE, computer sensors, Depth Anything and AprilTag workflows. Includes Objective-C++ bridge layers, platform APIs, native model/runtime integration and ongoing JUCE VST3/AU migration.
[Public product catalogue](https://ostinsolo.co.uk/devices)

### Real-Time Target-Speaker Voice Isolation — Private R&D
Real-time target-speaker extraction using MossFormer2 + ECAPA, with speaker enrollment and suppression of competing voices.

### SoundCloner — Private R&D
Native synthesis and audio-analysis research platform combining deterministic DSP, parameter/genome representations, similarity scoring, candidate retrieval, ML inference and large synthetic evaluation infrastructure.

### Sample-Space Exploration — Private R&D
CLAP/audio embeddings, classifier training, similarity retrieval and Three.js spatial exploration of audio corpora, supported by benchmark and evaluation tooling.

### iOS Computer Vision — Private R&D
Swift/SwiftUI iOS application work using ARKit, SceneKit, AVFoundation and MediaPipe Tasks Vision for real-time facial/eye landmark processing and guided physical-makeup workflows with simulator and physical-device validation.

## Engineering Validation

Repeatable benchmarking and regression methodology across projects: controlled baselines, latency/throughput profiling, held-out ML evaluation, parity testing, hardware-in-the-loop checks and cross-machine validation across Apple Silicon, Intel Mac and Windows x64/ARM64 execution paths where supported.

## Experience
### Founder & Audio Software Developer — VSTOPIA | 2023–Present
Built an independent software ecosystem spanning product development, web/backend infrastructure, distribution, licensing, updates and developer workflows.

### Independent Audio Software Developer — OSTIN SOLO | 2018–Present
Commercial and experimental audio technology across DSP, Max for Live, native Max externals, plug-ins, machine learning, computer vision, MPE/hardware control and networked music systems.

### Founder, Artistic Director & Experience Designer — Macrowave / Cacao Discoteca / Basement | 2014–2016
Directed electronic-music and multimedia programmes in Italy for audiences up to 3,000, spanning artist curation, production, projection mapping, scenography and interactive installations.


## Education
**Music Production — SAE Institute | 2019–2020** · Recording, editing, mixing, mastering, sound design and synthesis
**Spanish Language Studies — Valencia | 2022**
**Electronic Music & Musicianship — Italian Conservatory | c. 2004–2009**
**Scientific High School Diploma — Liceo Scientifico, Italy | c. 2007–2012**

## Languages
Italian — Native · English — Full professional proficiency, IELTS certified · Spanish — Professional working proficiency

## Recognition & Public Evidence
Sound On Sound coverage of DSm · Cycling ’74 official project listing · OSTIN SOLO commercial product catalogue · public AUDIOENCE platform and technical documentation.

**Full technical portfolio:** https://ostinsolo.github.io/ostin-solo-portfolio/
