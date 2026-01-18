# Arthemy_Live-Tuner-SDXL-ComfyUI
ComfyUI nodes useful to Tweak SDXL, Illustrious, and NAI models by adjusting specific 'slices'. These nodes break the U-Net and CLIP into areas of application (like Style, Lighting, Word Logic...) and use sliders to boost or lower the intensity of any of those sections without training.

---

# ✨ Arthemy Live Tuner - SDXL

Hi everyone!

After years of experimenting with SDXL (including all its variants like Illustrious and NAI) and diving deep into model merging, I developed these nodes to offer granular control over a single model.

In short, I took the complex logic of "SDXL Block Merging" and reorganized it into functional groups based on their actual visual impact on image generation. Instead of merging two models, these nodes act on a **single model**, allowing you to amplify or reduce the intensity of specific "slices" or areas of application.

The process is incredibly fast and can be added to any workflow, effectively transforming static checkpoints into a set of **"Model Sliders"** for total creative control.

---

## Key Features

* **Visual Equalizer:** Adjust the "volume" of specific model parts like Layout, Lighting, or Texture without changing the entire image.
* **No Retraining Required:** Get LoRA-like control directly on your base checkpoint.
* **Optimized for SDXL:** Deep support for the 32-layer CLIP (ViT-bigG) and U-Net architecture.
* **Compatible with Everything:** Works with SDXL, Illustrious, NAI, and most SDXL-based merges.

---

## The Nodes

### 1. ✨ Arthemy Model Live Tuner

This node targets the **U-Net** (the visual brain). I've grouped the technical blocks into intuitive sliders:

* **Structure & Composition:** Control the geometry, perspective, and global masses.
* **Subject & Core:** Fine-tune object semantics and the central heart of the image.
* **Style & Rendering:** Boost the art style, material substance, or lighting/atmosphere.
* **Fine Details:** Push high-frequency details like skin textures and final sharpness.

### 2. ✨ Arthemy CLIP Live Tuner

This node targets the **CLIP Text Encoder**, dividing it into 3 logical blocks to control how the AI "reads" your prompt:

* **Syntax Rigidity:** How strictly the AI follows your grammar and word order.
* **Semantic Focus:** How much weight is given to the objects and actions you describe.
* **Style Abstraction:** Control the level of artistic flair vs. literal interpretation.

---

## 🎚️ Tuning Modes: Soft vs. Real

You can choose between two mathematical curves for the sliders:

* **Real Value:** A direct, linear multiplier. If you set 1.2, the area is 20% stronger. Best for surgical precision.
* **Soft Value:** A custom quadratic curve designed for smoother transitions.
* Below 1.0, it uses  to prevent the model from "breaking" or collapsing too quickly.
* Above 1.0, it applies a gentler 0.133 scaling factor.
* **Use Soft Mode** for a more "organic" feel when you want to make subtle improvements.


---

## Installation

1. Navigate to your `ComfyUI/custom_nodes/` folder.
2. Run: `git clone https://github.com/aledelpho/Arthemy_Live-Tuner-SDXL-ComfyUI.git`
3. Restart ComfyUI.

---
