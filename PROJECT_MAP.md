# Project & Technology Map

A deliberately **wide, shallow portfolio map** designed to keep the architecture visible in one view. OSTIN SOLO sits at the top, the main engineering domains share one horizontal band, and each domain has a single compact project/technology band beneath it.

## Portfolio architecture

```mermaid
%%{init: {"flowchart": {"nodeSpacing": 16, "rankSpacing": 42, "curve": "linear", "htmlLabels": true}, "themeVariables": {"fontSize": "16px"}}}%%
flowchart TB
    O["OSTIN SOLO<br/><b>Audio × Software × ML × Interactive Systems</b>"]

    subgraph DOMAINS[" "]
      direction LR
      AML["AUDIO / ML<br/>& DSP"]
      NATIVE["NATIVE C++<br/>& PLUG-INS"]
      AI["VOICE / AI"]
      CV["VISION /<br/>INTERACTION"]
      CLOUD["CLOUD / WEB<br/>& PLATFORM"]
      NET["NETWORKED<br/>AUDIO"]
    end

    O --> AML
    O --> NATIVE
    O --> AI
    O --> CV
    O --> CLOUD
    O --> NET

    subgraph DETAILS[" "]
      direction LR
      AMLX["DSm · SoundCloner<br/>RoFormer · Sample Generator"]
      NATX["Max SDK · C/C++ · Objective-C++<br/>JUCE · VST3 / AU<br/>native ML + hardware bridges"]
      AIX["ASA · Voice Agent<br/>Voice Isolation → Denoising → VAD<br/>STT → LLM / Agent → DAW"]
      CVX["Klic · Depth Anything<br/>AprilTag · Cameras<br/>Projection Mapping"]
      CLOUDX["VSTOPIA · Backend<br/>Max Web · Three.js<br/>deployment · licensing"]
      NETX["AUDIOENCE — WebRTC · audio + MIDI · DAW sync<br/>Max/Jitter UDP/TCP Audio Streaming — Node.js"]
    end

    AML --> AMLX
    NATIVE --> NATX
    AI --> AIX
    CV --> CVX
    CLOUD --> CLOUDX
    NET --> NETX

    classDef root font-size:22px,font-weight:bold;
    classDef domain font-size:16px,font-weight:bold;
    class O root;
    class AML,NATIVE,AI,CV,CLOUD,NET domain;
    style DOMAINS fill:none,stroke:none
    style DETAILS fill:none,stroke:none
```

## Native systems depth

The **Native C++ & Plug-ins** branch includes work that is easy to lose when projects are described only by product name:

- C and C++ components wrapped for the **Max SDK**, including interfaces between Max object APIs and reusable native engines.
- **Objective-C++ bridge layers** used where C++ systems need access to Apple/macOS frameworks and platform-specific APIs.
- Native communication layers for **hardware, sensors and operating-system services**, including lower-level macOS integration used by the Max external family.
- Custom bridges and runtime/resource layouts for embedding and distributing **machine-learning models and native inference components** with Max externals.
- JUCE/C++ development targeting **VST3, Audio Unit and standalone** applications.
- **Apple Developer Program** distribution workflow: Developer ID signing, Hardened Runtime and notarization for independently distributed macOS software and plug-ins.

## Recurring engineering themes

- **C++ / native systems:** Max externals, JUCE plug-ins, Objective-C++ bridges, hardware APIs, computer vision and neural-audio runtimes.
- **Audio ML:** source separation, synthesis reconstruction, CLAP/audio embeddings, classification, retrieval and model evaluation.
- **Interactive systems:** multitouch/MPE, Three.js graph interfaces, cameras, AprilTags, projection mapping and physical sensors.
- **Evaluation engineering:** benchmarks, controlled experiments, profiling, parity/regression testing and quantitative model/system comparisons.
- **Productisation:** experimental systems progressing toward native externals, VST3/AU/standalone software, Apple signing/notarization, deployment, licensing and commercial distribution.

The map is architectural rather than chronological: the projects share reusable technologies and research methods instead of existing as isolated experiments.
