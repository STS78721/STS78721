# Hi there, I'm STS78721 👋
### Lead Developer & Maintainer of TotK Recomp: Next Gen STS Build

Welcome to my GitHub profile! I specialize in native static game recompilation, Vulkan graphics pipeline optimization, next-generation neural upscaling, and multi-frame generation.

---

## 🚀 Featured Project: [TotK Recomp — Next Gen STS Build](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild)

Static recompilation of *The Legend of Zelda: Tears of the Kingdom* to native Windows and Linux x86-64 with an advanced Vulkan rendering architecture.

### 🏆 [Beta 2: Next Gen STS Unified Build (v0.3.4-beta-2-steeltemple)](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild/releases/latest) is NOW LIVE!

#### 📋 Summary of Changes & Features in Beta 2:
- **Clean RTGI & Ray Reconstruction Removal**: Removed unpolished screen-space ray tracing and noisy denoisers, resulting in pristine image fidelity, zero temporal ghosting, and rock-solid framerates.
- **Intel XeGTAO Ground Truth Ambient Occlusion**: Full integration of Intel XeGTAO for micro-shadowing depth and contact shadow realism with negligible GPU overhead, alongside SSAO and HBAO.
- **Unified Upscaler Hub**: NVIDIA DLSS 4 / 4.5 Transformer presets (`K`, `J`, `M`, `L`), DLSS 3 CNN presets (`E`, `C`), DLAA, and AMD FSR 4.1.2 context-aware neural upscaling + FSR 1.0.
- **Next-Gen Multi-Frame Generation**: NVIDIA DLSS Frame Gen with up to 4x/6x Multi-Frame Generation (RTX 50-series gated), plus AMD FSR 3.1 & FSR 4 AI Frame Gen across modern Radeon GPUs (RX 9070 XT, RX 7900 XTX).
- **Ultra-Low Latency Pipeline**: Full native NVIDIA Reflex (`VK_NV_low_latency2`) and AMD Anti-Lag 2 (`VK_AMD_anti_lag`) frame pacing.
- **In-Game Settings Overhaul**: In-game menu (F1) rebranded as `Next Gen STS Build`, featuring dedicated **Graphics Settings** and **DLSS NR** preview tabs.
- **OLED HDR10 Calibration**: Dynamic peak brightness, exposure, and HUD white point tuning (`Vivid`, `Clarity`, `Custom`).

---

## 📥 Quick Links & Resources
- 💾 **[Download Beta 2 Release](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild/releases/latest)** (Full Installer & Drop-in Packages)
- 📖 **[DLSS & FSR DLL Installation Guide](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild/releases/tag/v0.3.4-beta-2-steeltemple)**
- 🛠️ **[Main Project Repository](https://github.com/STS78721/totk-pc-recomp-SteelTempleBuild)**

---

## 🔬 Current Development & Upcoming Features
- ⚡ **DLSS 5 Neural Rendering (DLSS-NR)**: Streamline integration for real-time radiance caching and transformer denoising.
- 🟦 **Intel Xe Suite**: Dynamic runtime support for Intel XeSS upscaling (`libxess.dll`), XeLL low latency, and XeFG frame generation.
- 📊 Active continuous benchmarking and testing across diverse desktop and handheld configurations.
