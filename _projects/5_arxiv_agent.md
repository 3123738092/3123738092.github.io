---
layout: page
title: Multi-Skill Pipeline for Daily arXiv Briefings
description: An "Orchestrator + Skills" agent for automated daily arXiv digestion, ranking, and reporting.
img: assets/img/5.jpg
importance: 5
category: project
---

**Advisor:** Prof. Enyan Dai, AI Thrust, HKUST(GZ) · **Feb 2026 – May 2026**

[**GitHub repository →**](https://github.com/3123738092/arxiv-research-agent)

- Designed an **Orchestrator + Skills** architecture where skills communicate only through versioned JSON files under `shared_data`, keeping modules fully decoupled.
- Implemented the unified orchestrator `arxiv_agent.py` with **serial pipeline execution, idempotent re-runs, and fast-fail short-circuit** when the data-collector returns zero papers.
- Built the **data-collector** skill: arXiv paper fetching, metadata extraction, 384-dim MiniLM embeddings, and the cosine-similarity paper graph & co-author graph consumed by the downstream ranker.
