# hstrystyle - Cinematic Historical Art Style LoRA (SD 1.5)

## 📖 Overview
`hstrystyle` is a custom-trained Low-Rank Adaptation (LoRA) model for Stable Diffusion 1.5 (optimized for the WebUI Forge ecosystem). Designed specifically to generate high-fidelity, atmospheric, and painterly assets for documentary visualizations, this model strips away flat digital rendering and forces a gritty, textured, traditional fine-art aesthetic. 

It excels at depicting heavy low-key dramatic lighting, visible thick brushstrokes, moody skies, fog, and historical realism with a muted, classic color palette.

---

## 📦 Repository Structure
This repository contains the core weights along with the original training configuration files for full reproducibility:
*   `hstrystyle_v1.safetensors`: The main LoRA model weights (26.5 MB).
*   `config_lora-20260417-234259.toml`: The dataset and hyperparameter training configurations.
*   `hstrystyle_v1_20260417-234259.json`: The metadata and activation key logs.

---

## ⚙️ Core Generation Settings
To:

| Parameter | Recommended Target Value |
| :--- | :--- |
| **Base Checkpoint** | `dreamshaper_8.safetensors` (Do not use photo-realistic base models) |
| **Dimensions** | `896 x 504` (Optimized for 16:9 YouTube cinematic widescreen) |
| **Trigger Word** | `hstrystyle` |
| **LoRA Tag & Weight** | `<lora:hstrystyle_v1:1.1>` (Scale between `0.9` and `1.3` to adjust texture strength) |

---

## 💡 The Golden Prompt Formula

For consistent generation passes, anchor your prompts using this specific structural order:

```text
[Trigger Word], [Subject & Action], [Environment/Background], [Texture/Lighting keywords], [LoRA Tag]
