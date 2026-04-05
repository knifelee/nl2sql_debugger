---
title: "A Survey of Text-to-SQL in the Era of LLMs: Where are we, and where are we going?"
venue: TKDE 2025 (also on arXiv as 2408.05109)
arXiv: https://arxiv.org/abs/2408.05109
pdf: /ref/2408.05109_NL2SQL_Survey_LLM_Era.pdf  (already in ref/ folder)
---

## Authors
Xinyu Liu, Shuyu Shen, Boyan Li, Peixian Ma, Runzhi Jiang, Yuxin Zhang,
Ju Fan, Guoliang Li, Nan Tang, Yuyu Luo

## Overview
The most comprehensive survey of NL2SQL in the LLM era as of 2025. Covers the full lifecycle of Text-to-SQL from four aspects: Model, Data, Evaluation, and Error Analysis. Organizes methods into three pipeline stages: Pre-Processing, Translation, and Post-Processing.

## Dimensions Studied
- Model: fine-tuning vs prompting (ICL, CoT, decomposition, agents)
- Data: training data collection, synthesis, augmentation
- Evaluation: multiple metrics and benchmarks
- Error Analysis: schema linking errors, SQL structure errors, value errors
- Pipeline stages: pre-processing / translation / post-processing

## What It Does NOT Cover
- Reflection setting as a primary axis (mentions post-processing/self-correction but does not categorize into 6 types)
- User prompt quality (good vs ambiguous intent) as an explicit dimension
- Schema cleanliness (clean vs dirty) as a systematic comparison axis
- Human-in-the-loop interaction types beyond passing mention

## Key Insights
- LLM-based methods dominate; fine-tuning remains competitive for domain-specific tasks
- Schema linking is the dominant source of errors
- Self-correction (post-processing) improves accuracy but adds token cost
- Open problems: robustness, efficiency, interpretability, data lake settings

## BibTeX
```bibtex
@article{liu2024nl2sqlsurvey,
  author    = {Xinyu Liu and Shuyu Shen and Boyan Li and others},
  title     = {A Survey of Text-to-{SQL} in the Era of {LLMs}: Where are we, and where are we going?},
  journal   = {IEEE Transactions on Knowledge and Data Engineering},
  year      = {2025},
  url       = {https://arxiv.org/abs/2408.05109}
}
```
