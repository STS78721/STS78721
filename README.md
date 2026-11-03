# Hi there, I'm STS78721 👋
### Lead Developer & Maintainer of TotK Recomp: Next Gen STS Build

Welcome to my GitHub profile! I specialize in native static game recompilation, Vulkan graphics pipeline optimization, neural upscaling, and multi-frame generation.

---

## 🚀 Featured Project: [TotK Recomp — Next Gen STS Build](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild)

Static recompilation of *The Legend of Zelda: Tears of the Kingdom* to native Windows and Linux x86-64 with an advanced Vulkan rendering architecture.

### 🏆 [Beta 3: Next Gen STS Unified Build (v0.3.4-beta-3-steeltemple)](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild/releases/latest) is NOW LIVE!

<p align="center">
  <img src="https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild/releases/download/v0.3.4-beta-3-steeltemple/totk_overlay_beta3_grouped_hud.png" alt="Next Gen STS Beta 3 Grouped HUD Overlay" width="95%">
</p>

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│ ● 123 FPS (Base 82)  1% 85  0.1% 80  8.2 ms                                            │
│ DLSS 4.5 · Preset M  [DLSS FG 6x]  [NR ACTIVE · Preset B]  | 1080p -> 4K | Reflex      │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

#### 📋 Summary of Key Upgrades in Beta 3 (Hotfix Included):
- **Cave Entrance & Low-Light Black Screen Flicker Elimination**: Fixed an issue where approaching or entering caves caused black screen flickering with upscalers active (both NVIDIA DLSS and AMD FSR). The G-buffer filter now strictly enforces the configured scene resolution (`s[0]`), preventing intermediate 960x540 volumetric fog passes from hijacking the upscaler pipeline, and requires the scaling pass to strictly target output display resolution (`o[0]`).
- **Physically Accurate Frame Generation Telemetry & OFA Overhead Modeling**: Replaced theoretical multipliers with real-world Optical Flow Accelerator (OFA) compute overhead modeling. The overlay exposes both generated frame rate and base cadence (`● [Net FPS] (Base [Base FPS])`), matching NVIDIA FrameView and PresentMon.
- **Full Intel Stack Integration (XeSS 2.0+, XeFG, XeLL)**: Full support for Intel XeSS 2.0+ with hardware **XMX Matrix Acceleration** on Intel Arc and universal **DP4a** fallback across all GPUs. Hardware-aware **Intel XeFG** multi-frame generation (`2x`, `3x`, `4x`) and **Intel XeLL** driver frame pacing. Official Intel DLLs (`libxess.dll`, `libxess_fg.dll`, `libxell.dll`, `libxess_dx11.dll`) bundled and supported via resilient multi-path dynamic loading.
- **DLSS Neural Reconstruction (DLSS-NR) Hardware Gating & Uncoupling**: DLSS-NR is now completely uncoupled from DLSS/FG models and presets (`TOTK_DLSS_PRESET` and `TOTK_DLSS_NR_PRESET` operate independently). Non-NVIDIA GPUs or missing DLLs are automatically grayed out in the menu with clear explanatory badges. Leverages fast Preset B (`NVSDK_NGX_DLSS_Hint_Render_Preset_B`).
- **Refined Zero-Duplication HUD Performance Overlay**: Clean grouped technological pipeline (`DLSS 4.5 · Preset M` -> `[DLSS FG 6x]` -> `[NR ACTIVE · Preset B]` -> `| 1080p -> 4K | Hybrid MV | Reflex`), dedicated frame pacing line (`● FPS 1% Low 0.1% Low ms`), zero redundant text.
- **0.1% and 1% Low Frametime Metrics**: Added real-time micro-stutter and frame pacing hitch detection to both compact overlay and full HUD table.
- **Strict Dynamic DLSS vs DLAA Separation**: Real-time resolution evaluation accurately selects between `DLSS 4.5` (active upscaling) and `DLAA 4.5` (native 100% anti-aliasing).
- **Depth-Guided Hybrid Motion Vectors & Live Visualizer**: Analytical camera reprojection combined with depth-guided temporal disocclusion tracking for dynamic actors, completely eliminating ghosting on Link, weapons, enemies, and arrows.
- **Intel XeGTAO Ground Truth Ambient Occlusion**: Full integration of Intel XeGTAO micro-shadowing depth and contact shadow realism alongside 24-step directional HBAO and SSAO.
- **Industry-Standard Graphics Settings Terminology**: Intuitive options and clear descriptions designed for the everyday gamer.
- **PS5 DualSense Controller Architectural Blueprint**: Complete architecture published for dynamic adaptive triggers (bow draw resistance and string snap release), 4-channel controller audio routing for archery sound effects, and dynamic in-game button prompt detection.
