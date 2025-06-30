# FaceForge
## Sketch-to-Face Generation with StyleGAN2

This project implements a deep learning pipeline that converts **sketch images** into **realistic face images** using a pretrained **StyleGAN2** generator and a custom **OME Encoder**. The encoder learns to predict latent style modifications from a sketch input to drive face synthesis.

---

## Overview

- **Model Architecture:**
  - **OME Encoder**: A ResNet-based encoder that takes a sketch and previous face as input and outputs latent `delta_w` vectors.
  - **StyleGAN2**: A pretrained generator (frozen) used for high-fidelity face synthesis.
  
- **Losses Used:**
  - **L2 Loss**: Pixel-level similarity.
  - **LPIPS Loss**: Perceptual similarity.
  - **Identity Loss**: Preserves identity using FaceNet features.

- **Dataset**: [CelebA-HQ 256x256 Resized](https://www.kaggle.com/datasets/badasstechie/celebahq-resized-256x256)

---

