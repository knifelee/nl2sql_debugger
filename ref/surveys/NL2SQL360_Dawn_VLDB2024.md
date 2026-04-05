---
title: "The Dawn of Natural Language to SQL: Are We Fully Ready?"
venue: PVLDB 2024 (Experiments, Analysis & Benchmarks)
arXiv: https://arxiv.org/abs/2406.01265
pdf: https://www.vldb.org/pvldb/vol17/p3318-luo.pdf
github: https://github.com/HKUSTDial/NL2SQL360
---

## Authors
Boyan Li, Yuyu Luo, Chengliang Chai, Guoliang Li, Nan Tang (HKUST, Tsinghua)

## Overview
NL2SQL360 is a comprehensive experimental study and testbed for fine-grained evaluation of NL2SQL solutions. It integrates existing benchmarks, a repository of NL2SQL models, and various evaluation metrics into a unified framework. It is the closest existing paper to the user's proposed survey.

## Dimensions Studied
- SQL complexity (Easy / Medium / Hard / Extra Hard)
- Application scenario (Business Intelligence, etc.)
- Benchmark diversity (Spider, BIRD, KaggleDBQA, WikiSQL, Spider-Realistic, Dr.Spider)
- Evaluation metrics (EX, EM, VES, QVT)

## What It Does NOT Cover
- Schema cleanliness (clean vs dirty) as an explicit axis
- User prompt quality (good vs ambiguous intent)
- Reflection setting (no reflection / LLM pre / human pre / LLM post / human post / IR-level)
- Human-in-the-loop interaction types

## Key Results
- SuperSQL achieves 87% EX on Spider and 62.66% EX on BIRD
- Fine-grained analysis shows JOIN and subquery remain hard across all models
- KaggleDBQA (real-world) remains far below Spider performance

## BibTeX
```bibtex
@article{li2024dawn,
  author    = {Boyan Li and Yuyu Luo and Chengliang Chai and Guoliang Li and Nan Tang},
  title     = {The Dawn of Natural Language to {SQL}: Are We Fully Ready?},
  journal   = {Proceedings of the VLDB Endowment},
  volume    = {17},
  number    = {11},
  pages     = {3318--3331},
  year      = {2024},
  url       = {https://arxiv.org/abs/2406.01265}
}
```
