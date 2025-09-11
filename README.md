<div align="center">

# TIDMG: Text-Image Driven Motion Generation

_A research implementation of my MSc dissertation (full title: **TIDMG: Text-Image Driven Motion Generation with Unified Attention and Adaptive Conditioning**)_

### A person got down and is crawling across the floor
![Crawling Demo](example/crawling_I.gif)

### A person walks forward with wide steps
![Walking Demo](example/walk_I.gif)

### 🎥 Demo: Running TIDMG Code
👉 [**Watch Demo Video on Google Drive**](https://drive.google.com/file/d/1xPU2J5OJysevHOSKSHXdy6j3jp9G9VS0/view?usp=drive_link)

</div>

---

## 📘 Project Overview

TIDMG (Text-Image Driven Motion Generation) is the implementation of my MSc dissertation project.  
It is a diffusion-based framework that generates 3D human motions from natural language prompts, with **optional scene image conditioning** to improve spatial plausibility.

**Key contributions**
- **Unified conditioning**: supports both text and image inputs for scene-consistent motion generation.  
- **Combined Attention Block (CAB)**: merges self- and cross-attention into a single efficient operation.  
- **Adaptive LayerNorm (AdaLN)**: refines conditioning using timestep and text summary embeddings.  
- **Prompt normalization**: a lightweight LLM improves robustness to diverse natural language inputs.  

**Results (summary)**  
On HumanML3D and a curated scene-augmented subset, TIDMG achieves:
- Better semantic alignment (higher R-Precision, lower Multimodal Distance)  
- Improved diversity and multimodality of generated motions  
- Lower compute cost vs. separate self/cross attention stacks  

This repository provides demo scripts, visualization tools, and instructions to reproduce results.

---

## 📦 Demo & Dataset

- **Scene subset (images / configs / demo video)**:  
  👉 **[Google Drive Folder](http://google.com/drive/u/0/folders/1PjbXxfaFSeDkgsR7ml3aRiVnTD6GNjP3)**

- **HumanML3D (official data source for text–motion pairs)**:  
  👉 **[Kaggle: HumanML3D](https://www.kaggle.com/datasets/mrriandmstique/humanml3d)**

> Access tips  
> • Set the Drive folder permission to **“Anyone with the link – Viewer”**.  
> • HumanML3D is large and licensed — **do not redistribute raw data** here; download from Kaggle and follow their terms.

**Local path config (example)**
```text
DATA_ROOT=/path/to/HumanML3D
SCENE_ROOT=/path/to/scene_subset   # if you download the Drive scene data locally
CHECKPOINTS=./save/humanml_trans_enc_512/
OPTS=./assets/humanml_opt.txt
