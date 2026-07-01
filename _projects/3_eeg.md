---
layout: page
title: Brain-to-Image Retrieval & Reconstruction on THINGS-EEG2
description: Hierarchical Visual Features (HVF) pipeline fusing CLIP + SD-VAE + DINOv2 for EEG-based visual decoding.
img: assets/img/3.jpg
importance: 3
category: research
---

**Advisor:** Prof. Chen Liang, AI Thrust, HKUST(GZ) · **Feb 2026 – May 2026**

[**GitHub repository →**](https://github.com/3123738092/EEG-to-Image-Retrieval-Reconstruction)

- Designed the **Hierarchical Visual Features (HVF)** pipeline fusing CLIP RN50, CLIP ViT-B/32, and the Stable Diffusion VAE into a single regression target for the EEG encoder.
- Replaced plain-sum fusion with a **sigmoid-gated fusion** (bias init +3.0), letting the model attenuate unhelpful encoders — materially improved Top-5 / Top-10 / Mean Rank.
- Added a fourth encoder (**DINOv2 ViT-S/14 fine-tuned on Depth Anything V2**) to inject a 3D/depth prior missing from purely semantic features.
