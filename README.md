# 🎨 PBR Texture Tools: Normal & ORM Generator

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Web%20Browser-success.svg)](#)
[![Author](https://img.shields.io/badge/Author-Ashwath%20Jain-orange.svg)](https://github.com/ashwathjain)
[![Three.js](https://img.shields.io/badge/3D%20Preview-Three.js-black.svg)](https://threejs.org/)

> **A fast, standalone, in-browser texture generator for 3D artists and game developers.**  
> Effortlessly generate high-quality **Normal Maps** and packed **ORM (Ambient Occlusion, Roughness, Metallic) Maps** from any texture or image in real time—with zero installation, zero server dependencies, and live 3D preview.

---

## 👨‍💻 Created By
**Ashwath Jain**  
- **GitHub:** [@ashwathjain](https://github.com/ashwathjain)  
- **Email:** [jainashwath2002@gmail.com](mailto:jainashwath2002@gmail.com)

---

## 🌟 Highlights & Features

### 1. ⚡ Standalone & Zero-Setup
- **Runs completely in the browser**: No Node.js, Python, or command-line compilation required.
- **Client-Side Processing**: All texture computations happen locally on your GPU/CPU via the HTML5 Canvas API. Your images never leave your machine.
- Cross-platform launchers included for Windows (`Launch_Tool.bat`) and macOS (`Launch_Tool.command`).

### 2. 🗺️ High-Quality Normal Map Generation
- **Sobel / Gradient Filtering**: Converts height & luminance into tangent-space normal vectors.
- **Adjustable Intensity & Blur**: Fine-tune surface depth and smooth out high-frequency noise.
- **DirectX vs. OpenGL**: Support for standard and inverted green channel (-Y / +Y) workflows.

### 3. 📦 Packed ORM Map Creation
- Generates industry-standard packed ORM textures used across modern game engines (Unreal Engine, Unity, Godot, Blender):
  - **R Channel (Red):** Ambient Occlusion (AO)
  - **G Channel (Green):** Roughness
  - **B Channel (Blue):** Metallic

### 4. 🔲 Proportional Shape Edge Masking
- **Shape Modes**: Auto Island detection, Cube / Box projection, and Circle / Cylinder projection.
- **Edge Inset & Fade**: Eliminate ugly normal seam bleeding along UV boundaries.
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

## 🚀 Quick Start

### Option A: Windows
Double-click **`Launch_Tool.bat`** (or open `index.html` / `Texture_ORM_Normal_Generator.html` in Chrome, Edge, Firefox, or Brave).

### Option B: macOS
Double-click **`Launch_Tool.command`** (or open `index.html` / `Texture_ORM_Normal_Generator.html` in Safari or Chrome).

### Option C: Direct Browser / GitHub Pages
Simply open **`index.html`** or host this repository directly using **GitHub Pages** for instant access anywhere.

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
├── index.html                           # Main web entrypoint (GitHub Pages ready)
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
