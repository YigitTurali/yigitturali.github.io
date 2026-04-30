---
layout: page
title: PANINI / Generative Semantic Workspace
description: Continual learning in token space via structured memory (ICML 2026)
img: assets/img/1.jpg
importance: 1
category: research
related_publications: true
---

**PANINI** is a non-parametric continual-learning framework that encodes documents into **Generative Semantic Workspaces (GSW)** — entity- and event-aware networks of atomic question–answer (QA) pairs that enable reasoning-grounded inference over stored experience without continual parameter updates.

## What we built

- **Reasoning Inference Chain Retrieval (RICR):** a beam-search procedure that performs one-shot query decomposition and follows multi-hop inference chains through GSWs to assemble compact evidence.
- **Dual indexing for scalable memory access:** a BM25 index over entity + role/state descriptors paired with a dense vector index over QA pairs, enabling targeted retrieval of QA evidence rather than long text chunks.
- **End-to-end open-source pipeline:** GSW construction → retrieval → answering, supporting reproducible multi-hop QA.

## Headline results

- Top average performance across **six QA benchmarks**.
- **2–30× fewer** answer-context tokens than competitive baselines.
- Improved reliability via reduced unsupported answers on curated unanswerable queries.

> Accepted as a poster at **ICML 2026**. Co-authored with S. Rajesh, P. S. Holur, C. Duan, and V. Roychowdhury.
