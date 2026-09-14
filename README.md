# 🎨 PBR Texture Tools: Normal & ORM Generator

[![Live Tool](https://img.shields.io/badge/Live_Tool-Open_in_Browser-00c853?style=for-the-badge&logo=googlechrome&logoColor=white)](https://ashwathjain.github.io/PBR-Texture-Tools/)
[![Cocos Creator](https://img.shields.io/badge/Optimized_for-Cocos_Creator_3D-00A4FF?style=flat)](https://www.cocos.com/en/creator)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Web%20Browser-success.svg)](#)
[![Author](https://img.shields.io/badge/Author-Ashwath%20Jain-orange.svg)](https://github.com/ashwathjain)
[![Three.js](https://img.shields.io/badge/3D%20Preview-Three.js-black.svg)](https://threejs.org/)

> **A fast, standalone, in-browser texture generator built for Cocos Creator and 3D game developers.**  
> Effortlessly generate high-quality **Normal Maps** and packed **ORM (Ambient Occlusion, Roughness, Metallic) Maps** directly compatible with **Cocos Creator 3.x PBR materials** (as well as Unity, Unreal Engine, Godot, and Blender) in real time—with zero installation, zero server dependencies, and live 3D preview.

---

## 🚀 One-Click Web Tool

👉 **[Launch PBR Texture Tools Online](https://ashwathjain.github.io/PBR-Texture-Tools/)**  
*(Double-click the link above to immediately run the generator right in your web browser — no download or installation required!)*

---

## 👨‍💻 Created By
**Ashwath Jain**  
- **GitHub:** [@ashwathjain](https://github.com/ashwathjain)  
- **Email:** [jainashwath10@gmail.com](mailto:jainashwath10@gmail.com)

---

## 🥥 Optimized for Cocos Creator (Cocos 3D)

This tool is specifically tailored to streamline the texture workflow for **Cocos Creator 3.x**:

1. **Native ORM Channel Packing:**
   Cocos Creator's standard PBR material pipeline utilizes a single packed texture for occlusion, roughness, and metallic properties to optimize draw calls and memory bandwidth:
   - **R (Red Channel):** Ambient Occlusion (AO)
   - **G (Green Channel):** Roughness
   - **B (Blue Channel):** Metallic
2. **Direct Slot Assignment in Cocos Creator:**
   - Drop your diffuse/albedo texture into this tool.
   - Adjust intensity, blur, and edge masking to match your model's geometry.
   - Click **Download Both Maps**.
   - Drag `<name>_Normal.png` directly into the **NormalMap** slot in the Cocos Creator Material Inspector.
   - Drag `<name>_ORM.png` directly into the **OcclusionRoughnessMetallicMap** slot in Cocos Creator.
   - Set PBR shading parameters and you're ready to render!

---

## 🌟 Highlights & Features

### 1. ⚡ Standalone & Zero-Setup
- **Runs completely in the browser**: No Node.js, Python, or command-line compilation required.
- **Client-Side Processing**: All texture computations happen locally on your GPU/CPU via the HTML5 Canvas API. Your images never leave your machine.
- Cross-platform launchers included for Windows (`Launch_Tool.bat`) and macOS (`Launch_Tool.command`).
- Ready for 1-click web execution via [GitHub Pages](https://ashwathjain.github.io/PBR-Texture-Tools/).

### 2. 🗺️ High-Quality Normal Map Generation
- **Sobel / Gradient Filtering**: Converts height & luminance into tangent-space normal vectors.
- **Adjustable Intensity & Blur**: Fine-tune surface depth and smooth out high-frequency noise.
- **DirectX vs. OpenGL**: Support for standard and inverted green channel (-Y / +Y) workflows.

### 3. 📦 Packed ORM Map Creation
- Generates industry-standard packed ORM textures for **Cocos Creator**, Unreal Engine, Unity, Godot, and Blender:
  - **R Channel (Red):** Ambient Occlusion (AO)
  - **G Channel (Green):** Roughness
  - **B Channel (Blue):** Metallic

### 4. 🔲 Proportional Shape Edge Masking
- **Shape Modes**: Auto Island detection, Cube / Box projection, and Circle / Cylinder projection.
- **Edge Inset & Fade**: Eliminate normal seam bleeding along UV boundaries.
- **Mask Strength & Outside Opacity**: Precise control over inner vs. outer texture regions.

### 5. 🖌️ In-Browser Normal Canvas Editor
- Built-in pop-up editor for manual touch-ups:
  - **🧹 Erase Normal Brush**: Softly or completely flatten unwanted bumps back to neutral flat normal `(128, 128, 255)`.
  - **↩️ Restore Normal Brush**: Paint back calculated normal map details.
  - **Base Texture Overlay**: Fade your source texture underneath for exact alignment and tracing.
  - **Zoom & Pan Canvas**: Full viewport control with hotkeys.

### 6. 🎮 Interactive Live 3D Viewport
- Real-time WebGL rendering powered by **Three.js**.
- Swap 3D preview meshes instantly: **Cube**, **Cylinder**, **Sphere**, or **Plane**.
- Orbit controls: Left-click drag to rotate, right-click/middle-click to pan, scroll wheel to zoom.
- See your base texture, normal map, and ORM map rendered with physically based lighting in real time.

### 7. 💾 One-Click Export
- Export `<name>_Normal.png`
- Export `<name>_ORM.png`
- Batch export both maps simultaneously with a single click.

---

## 🚀 Quick Start Options

### Option 1: 🌐 Online (One-Click)
Open **[ashwathjain.github.io/PBR-Texture-Tools](https://ashwathjain.github.io/PBR-Texture-Tools/)** directly in any modern browser.

### Option 2: 🪟 Windows (Local)
Double-click **`Launch_Tool.bat`** in the repository folder.

### Option 3: 🍎 macOS (Local)
Double-click **`Launch_Tool.command`** in the repository folder.

---

## ⌨️ Canvas Editor Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| **Space + Drag** / **Middle Click** | Pan canvas |
| **Scroll Wheel** | Zoom in / out |
| **[** / **]** | Decrease / Increase brush size |
| **B** | Select Erase Normal brush |
| **E** | Select Restore Normal brush |
| **ESC** | Close Editor modal |

---

## 📁 Repository Structure

```text
PBR-Texture-Tools/
├── index.html                           # Main web entrypoint (GitHub Pages live tool)
├── Texture_ORM_Normal_Generator.html    # Standalone generator application
├── Launch_Tool.bat                      # 1-Click launcher for Windows
├── Launch_Tool.command                  # 1-Click launcher for macOS
├── LICENSE                              # MIT License
└── README.md                            # Documentation & user guide
```

---

## 🛠️ Tech Stack
- **HTML5 Canvas 2D API** (Pixel manipulation & convolution kernels)
- **Three.js (r128)** (Real-time PBR material rendering & OrbitControls)
- **Vanilla JavaScript & Modern CSS** (Zero external runtime dependencies)

---

## 📄 License
This project is open source and available under the [MIT License](LICENSE).

Copyright (c) 2026 **Ashwath Jain**.
