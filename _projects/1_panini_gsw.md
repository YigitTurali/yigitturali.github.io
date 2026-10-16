---
layout: page
title: PANINI-DR / PANINI / Generative Semantic Workspace
description: Deep-research agents (PANINI-DR) and continual learning (PANINI, ICML 2026) via structured memory
img: assets/img/1.jpg
importance: 1
category: research
related_publications: true
---

**Generative Semantic Workspaces (GSW)** are entity- and event-aware structured memories built from atomic question–answer (QA) pairs. This research thread uses them for deep-research agents (**PANINI-DR**) and for non-parametric continual learning (**PANINI**).

## PANINI-DR: controlled deep research

[Paper (arXiv:2610.15208)](https://arxiv.org/abs/2610.15208) · [Code](https://github.com/roychowdhuryresearch/panini-dr) · [Project page](https://roychowdhuryresearch.github.io/PANINI-DR_Project_Page/)

**PANINI-DR** is a multi-agent deep-research harness that separates coordination of the overall investigation from the research and verification of individual subquestions.

- **Shared GSW workspace:** records subquestions, their dependencies, findings, and supporting evidence, so agents work from explicit research state instead of long chat histories.
- **Verification agent:** checks proposed answers against their subquestions and evidence; verification feedback guides further investigation.
- **Results:** strongest average performance on BrowseComp-Plus, FRAMES, and MoNaCo against seven baselines with a shared language-model backbone and frozen corpora. **73.3%** accuracy on BrowseComp-Plus, **16.0 points** above the next-best baseline, and 26 of 50 hard questions answered correctly, nearly twice the next-best baseline. It also achieves the highest answer recoverability from saved evidence on all three benchmarks.

> Under review at **ICLR 2027**. Co-first authors M. Y. Turali and S. Rajesh, with M. E. Lorasdagi, C. Duan, K. Sharma, and V. Roychowdhury.

## PANINI: continual learning in token space

[Paper (arXiv:2602.15156)](https://arxiv.org/abs/2602.15156) · [Code](https://github.com/roychowdhuryresearch/gsw-memory)

**PANINI** is a non-parametric continual-learning framework that encodes documents into GSWs, enabling reasoning-grounded inference over stored experience without continual parameter updates.

- **Reasoning Inference Chain Retrieval (RICR):** a beam-search procedure that performs one-shot query decomposition and follows multi-hop inference chains through GSWs to assemble compact evidence.
- **Dual indexing for scalable memory access:** a BM25 index over entity + role/state descriptors paired with a dense vector index over QA pairs, enabling targeted retrieval of QA evidence rather than long text chunks.
- **Results:** top average performance across **six QA benchmarks** with **2–30× fewer** answer-context tokens than competitive baselines, and fewer unsupported answers on curated unanswerable queries.

> Accepted as a poster at **ICML 2026**. Co-authored with S. Rajesh, P. S. Holur, C. Duan, and V. Roychowdhury.
