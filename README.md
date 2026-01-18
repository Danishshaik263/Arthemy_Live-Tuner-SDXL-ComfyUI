# Arthemy_Live-Tuner-SDXL-ComfyUI
ComfyUI nodes useful to Tweak SDXL, Illustrious, and NAI models by adjusting specific 'slices'. These nodes break the U-Net and CLIP into areas of application (like Style, Lighting, Word Logic...) and use sliders to boost or lower the intensity of any of those sections without training.

🎚️ Arthemy Live Tuner: The SDXL Equalizer
Hi everyone!

After years of experimenting with SDXL (and all its variants) and model merging, I developed these nodes to offer granular control over individual models.

In short, I took the same block-splitting system used in "SDXL Block Merging" tools and reorganized it into logical groups based on the parts of the generation they influence most visibly. Instead of merging two models, these nodes work on a single model, allowing you to amplify or reduce the intensity of specific "slices" in real-time.

It’s a very fast process that fits into any workflow, turning static models into "Slider-based Models" to give you total control over how a checkpoint performs.

🚀 What does it do?
Imagine your model is an audio track. Usually, you can only turn the volume up or down (the strength of a LoRA or Checkpoint). Arthemy Live Tuner is the equalizer. Want more detail but less "lighting" influence? Just move the sliders.

🧠 Arthemy Model Tuner (U-Net)
This node breaks down the U-Net into semantic areas:

Layout & Geometry: Controls the "bones" and spatial structure.

Subject Identity: Defines the semantic heart of objects and characters.

Art Style & Medium: The main driver for the artistic look.

Atmosphere & Lighting: Adjusts volumetrics and light behavior.

Texture & Sharpness: Fine-tunes high-frequency details like skin pores or fabric.

✍️ Arthemy CLIP Tuner
Controls how the AI interprets your words:

Syntax Rigidity: How strictly the AI follows your grammar.

Semantic Focus: How much weight is given to the objects/actions described.

Style Abstraction: How much the "artistic vibe" overrides literal prompt adherence.

⚖️ Real Value vs. Soft Value
I’ve included two modes to handle how the weights are applied:

Real Value: A direct, linear multiplier. If you set it to 1.5, the weight of those blocks increases by exactly 50%. Best for surgical precision.

Soft Value: This uses a custom quadratic curve. It’s designed to be "safer" and smoother. It prevents the model from "breaking" or over-saturating too quickly when you push the sliders to extremes, making transitions feel more natural.

🖼️ Visual Guide (Where to add images)
To make this README truly "pop," I suggest adding images in these specific spots:

Header Image: Right under the main title.

What to show: A screenshot of both nodes (Model and CLIP Tuner) connected to a Load Checkpoint node in ComfyUI.

The "Equalizer" Effect: Under the "What does it do?" section.

What to show: A Comparison Grid (XY Plot). Take the same seed and prompt, then show 3 versions:

Subject Identity at 0.5.

Subject Identity at 1.0 (Default).

Subject Identity at 1.5.

Texture Control: Under the "Model Tuner" description.

What to show: A close-up (crop) of a face or fabric. Show the difference between OUT_Texture_Details at 0.8 vs 1.4. This highlights the "sharpness" control without using external filters.

CLIP Logic: Under the "CLIP Tuner" section.

What to show: An image with a complex prompt. Show how Style Abstraction at 1.5 makes the image more "painterly/vibrant" even if the prompt is simple.

🛠️ Installation
Navigate to your ComfyUI/custom_nodes/ folder.

Run: git clone https://github.com/aledelpho/Arthemy_Live-Tuner-SDXL-ComfyUI.git

Restart ComfyUI.
