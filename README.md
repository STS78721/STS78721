# Hi there, I'm STS78721 👋
### Lead Systems & Graphics Programmer | Native Static Recompilation & Vulkan Architecture

[![GitHub Release](https://img.shields.io/github/v/release/STS78721/totk-pc-recomp-SteelTempleBuild?color=ffd24d&label=Latest%20Release&style=for-the-badge)](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20x86--64-blue?style=for-the-badge)](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild)
[![Vulkan](https://img.shields.io/badge/Vulkan-1.3%20%2F%201.4%20Native-red?style=for-the-badge&logo=vulkan)](https://www.vulkan.org/)
[![NVIDIA](https://img.shields.io/badge/NVIDIA-DLSS%20%7C%20DLSS--NR%20%7C%20Reflex-76b900?style=for-the-badge&logo=nvidia)](https://developer.nvidia.com/)

Welcome! I specialize in **ahead-of-time (AOT) static game recompilation**, **low-level Vulkan rendering systems (NVN & NVN 2 host translations)**, **neural rendering architectures (DLSS-NR Pre-SR)**, **multi-frame generation (MFG)**, and **driver-level input latency synchronization**.

---

## 🚀 Flagship Project: [TotK Recomp — Next-Gen STS Build](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild)

A high-performance, native PC port of *The Legend of Zelda: Tears of the Kingdom* engineered for native x86-64 execution with cutting-edge graphics technology.

### 🏆 [Beta 6: DLSS Neural Rendering (Pre-SR Multipass) & Hardened Frame Generation](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild/releases/tag/Beta-6) is NOW LIVE!

<p align="center">
  <img src="https://raw.githubusercontent.com/STS78721/totk-pc-recomp-SteelTempleBuild/main/launcher/launcher_showcase.png" alt="SteelTemple Standalone Launcher" width="92%">
</p>

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ ● 240 FPS (Base 120)  1% 210  0.1% 185  4.2 ms                                         │
│ DLSS 4K  [FG 6x]  [NR Active · Preset B]  | 1080p -> 4K | Reflex Boost                 │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### 🌟 Flagship Innovations in Beta 6:
* **🧠 Native OptiScaler-Style Pre-SR Multipass Pipeline:**
  * **Stage 1 (Pre-SR Neural Denoising & Reconstruction):** DLSS Neural Rendering (Preset B) evaluates directly at native render resolution across sequential passes (`1x`, `2x`, `3x`, `4x`), resolving complex specular reflections, micro-shadows, and foliage chatter directly on Tensor Cores.
  * **Stage 2 (Super Resolution AI Upscaling):** Clean reconstructed frames feed straight into DLSS Super Resolution (Feature 1, Preset M), cleanly upscaling to razor-sharp native 4K (`3840x2160`).
* **🛡️ Shadow Cascade Camera Jitter Fix:** Isolated camera viewport Halton jitter during neural rendering passes, completely eliminating shadow cascade flickering while preserving full temporal stability.
* **⚡ Blackwell RTX 50 Multi-Frame Generation (MFG):** Native frame interpolation supporting `2x`, `3x`, `4x`, and `6x` multipliers, validated and hardened for NVIDIA GeForce RTX 50 Series (Blackwell) architectures.
* **⚡ NVIDIA Reflex (`VK_NV_low_latency2`):** Complete 6-point latency marker loop (`SIMULATION_START` through `PRESENT_END`) with Boost mode pinned GPU clocks for minimal input lag.
* **🎮 Standalone Sony/Nixxes-Inspired PC Launcher (`TotKLauncher.exe`):**
  * Built-in 1-Click Mod Manager with automatic `.zip` / `.rar` / `.7z` archive extraction and GameBanana mod browser integration.
  * Automatic 4K texture pack heap detection (`HeapDef.byml.zs`) and memory expansion.
  * Interactive Save Backup Vault with pre-restore snapshots and process guard.
* **🖥️ Ultrawide HUD Auto-Patcher:** Dynamic in-place decompression, coordinate transformation, and recompression of custom button prompt mods (`Common.Product.*.blarc.zs`) for flawless 21:9 and 32:9 gameplay.

---

## 🔬 Next-Gen & Switch 2 Static Recompilation R&D

Beyond *Tears of the Kingdom*, I develop and maintain cutting-edge static recompilation research projects targeting next-generation console architectures and native Vulkan graphics backends:

| Project | Target Title / Architecture | Status & Highlights | Repository |
| :--- | :--- | :--- | :--- |
| **🏎️ MKW-THWOMP** | *Mario Kart World*<br>*(Nintendo Switch 2)* | **Active R&D (24 ⭐)**<br>Static recompilation translating ARM64 code into native Windows x86-64 with Vulkan. 3D intro rendering and host NVN 2 pipeline initialization. | [STS78721/MKW-THWOMP](https://github.com/STS78721/MKW-THWOMP) |
| **🎾 MTF-ShadowRacket** | *Mario Tennis Fever*<br>*(Nintendo Switch 2)* | **Early Boots & Pipeline Bringup**<br>First public static recompilation of *Mario Tennis Fever*. Horizon OS initialization, 6 guest threads across cores, and host NVN 2 Vulkan implementation. | [STS78721/MTF-ShadowRacket](https://github.com/STS78721/MTF-ShadowRacket) |
| **🍌 dkb-BANANAS** | *Donkey Kong Bananza*<br>*(Nintendo Switch 2)* | **Tutorial Rendered (9 ⭐)**<br>Native static recompilation to Windows with Vulkan. 3D tutorial world and asset streaming verified. | [STS78721/dkb-BANANAS](https://github.com/STS78721/dkb-BANANAS) |
| **🗡️ OOT-MASTERSWORD** | *Zelda: Ocarina of Time*<br>*(Switch 2 Remake)* | **In Progress**<br>Static recompilation exploring modernized rendering passes, high-resolution geometry, and native input bindings. | [STS78721/OOT-MASTERSWORD](https://github.com/STS78721/OOT-MASTERSWORD) |
| **⏳ OOT-FOREVER** | *Zelda: Ocarina of Time*<br>*(PC Native)* | **Native PC Execution**<br>Zero-emulation standalone Windows implementation built from legal game dumps with unlocked framerates. | [STS78721/OOT-FOREVER](https://github.com/STS78721/OOT-FOREVER) |

---

## 🤝 Upstream Core Contributions ([valentderah/totk-pc-recomp](https://github.com/valentderah/totk-pc-recomp))

* **NVIDIA Reflex Low Latency Engine Integration ([PR #638](https://github.com/valentderah/totk-pc-recomp/pull/638) & [PR #913](https://github.com/valentderah/totk-pc-recomp/pull/913)):**
  Authored the official NVIDIA Reflex (`VK_NV_low_latency2`) implementation for the upstream project, carried and rebased against the latest upstream development tree by core maintainers.
* **Environmental Physics & Fire Spread Fix:**
  Identified and resolved environmental fire propagation timing desync in the recompilation engine (credited in upstream v0.3.10).

---

## 🛠️ Technical Stack & Specialties

| Domain | Technologies & Frameworks |
| :--- | :--- |
| **Languages** | C, C++20, Python 3.12+, HLSL, GLSL, ARM64 / x86-64 Assembly |
| **Graphics APIs** | Vulkan 1.3 / 1.4, DirectX 12, SPIR-V Compute Shaders, NVN & NVN 2 Host Translation |
| **Neural AI & Upscaling** | NVIDIA NGX (DLSS 4.5, DLSS-NR Preset B, DLSS-G, Reflex), AMD FidelityFX (FSR 3.1, FSR 4 AI FG, Anti-Lag 2), Intel XeSS 2.0+ (XMX & DP4a, XeFG, XeLL) |
| **Shading & Lighting** | Intel XeGTAO Ground Truth Ambient Occlusion, Contact Shadows, Dynamic AO (HBAO/SSAO), HDR10 |
| **System Engineering** | AOT binary lifting, high-performance multithreading, lockless ring buffers, VMA, reverse engineering |

---

### 📬 Connect & Repositories

* **Main Repository:** [STS78721/totk-pc-recomp-SteelTempleBuild](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild)
* **Latest Standalone Release:** [Download Beta 6](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild/releases/tag/Beta-6)
