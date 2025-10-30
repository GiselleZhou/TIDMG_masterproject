<div align="center">

# TIDMG: Text-Image Driven Motion Generation

_A research implementation of my MSc dissertation (full title: **TIDMG: Text-Image Driven Motion Generation with Unified Attention and Adaptive Conditioning**)_

### A person got down and is crawling across the floor
![Crawling Demo](example/crawling_I.gif)

### A person walks forward with wide steps
![Walking Demo](example/walk_I.gif)


---

### Codes

Because the codes files are too much and keep failed when uploading on github(probably because of the Chinese Internet), I put the codes in the drive folder.
[**Get the Codes on Google Drive**](https://drive.google.com/drive/folders/1Hycy0FFxAuoYMY7_htfN0C3LDuoO7sid?usp=drive_link)


---

### 🎥 Demo: Running TIDMG Code
👉 [**Watch Demo Video on Google Drive**](https://drive.google.com/file/d/1kbeGlJqJrZdj9OJJETQYtZ6P0EJO8G2r/view?usp=sharing)




---

## 📄 Thesis
[Read the full dissertation (PDF)](TIDMG_paper.pdf)

---

## 📘 Project Overview


TIDMG is my MSc project: a diffusion-based model that turns text—optionally with a scene image—into 3D human motion using unified conditioning, a single-pass attention block, and AdaLN. On HumanML3D and a small scene subset it improves alignment/diversity and lowers compute. This repo includes quick demos, visualization, and setup instructions.



---

## 📦 Dataset

- **Scene subset (scene images dataset / demo video)**:  
  👉 **[Google Drive Folder](### 🎥 Demo: Running TIDMG Code
👉 [**Get the Scene Dataset on Google Drive**](https://drive.google.com/drive/folders/1DpqCr_h2FyTUEWEhVeBfKHTtq7GMW8qW?usp=drive_link)
)**

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
