---
layout: page
title: Ascend C Custom Operators on Atlas 910B
description: Scale & Atanh AI Core kernels with generalized tiling and dtype-specialized dispatch — Outstanding Prize, Ascend S8.
img: assets/img/8.jpg
importance: 8
category: project
---

**Ascend AI Innovation Contest Season 8** · **Outstanding Prize** · Jun 2026

[**GitHub repository →**](https://github.com/3123738092/Ascend_S8)

- Implemented **Scale** and **Atanh** operators as custom AI Core kernels in **Ascend C** using msopgen-generated `op_host` (Tiling + InferShape + prototype registration) and `op_kernel` projects on the Atlas 910B (aarch64) platform.
- Designed generalized tiling strategies covering **arbitrary rank inputs (1D / 2D / 4D / 6D)** with **non-32-aligned tail** handling.
- Used **dispatch** technology to specialize kernels per dtype (**fp16 / bf16 / fp32**) and shape regime.
