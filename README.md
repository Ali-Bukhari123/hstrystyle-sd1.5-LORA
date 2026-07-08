# hstrystyle - Cinematic Historical Art Style LoRA (SD 1.5)

## 📖 Overview
`hstrystyle` is a custom-trained Low-Rank Adaptation (LoRA) model for Stable Diffusion 1.5 (optimized for the WebUI Forge ecosystem). Designed specifically to generate high-fidelity, atmospheric, and painterly assets for documentary visualizations, this model strips away flat digital rendering and forces a gritty, textured, traditional fine-art aesthetic. 

It excels at depicting heavy low-key dramatic lighting, visible thick brushstrokes, moody skies, fog, and historical realism with a muted, classic color palette.

🎨 Style Examples

<img width="1024" height="567" alt="image" src="https://github.com/user-attachments/assets/a8a30051-7004-4b4c-a9a8-d3c549035489" />
<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/39b722b3-a28a-4b73-b5d2-1485cff9fc77" />
<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/063cfdbd-2c89-4f12-adf5-8191b05f4bce" />
<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/e832b5e0-1fa6-4a87-98f4-99d8ae008d20" />
<img width="512" height="640" alt="image" src="https://github.com/user-attachments/assets/603ec91b-fe47-45d2-99c4-c2d471a3b11e" />
<img width="512" height="640" alt="image" src="https://github.com/user-attachments/assets/08a6cf0e-caf0-4bd3-820e-a807a6f1f297" />
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/6c1d942b-5eed-4d12-adad-3d87661c8126" />
<img width="512" height="640" alt="image" src="https://github.com/user-attachments/assets/815ec99f-b784-4dc5-bce8-e94758a6b7c4" />



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
