---
title: "Natural Language to SQL: State of the Art and Open Problems"
venue: PVLDB 2025
doi: https://dl.acm.org/doi/10.14778/3750601.3750696
pdf: https://www.vldb.org/pvldb/vol18/p5466-luo.pdf
---

## Authors
Yuyu Luo, Guoliang Li, Ju Fan, Chengliang Chai, Nan Tang

## Overview
A concise state-of-the-art overview published in PVLDB 2025 (Vol. 18, No. 12, pp. 5466–5471). Summarizes the current landscape of NL2SQL methods and identifies open problems for future research. Shorter in scope than the TKDE survey but more up to date.

## Dimensions Studied
- Current best-performing methods and benchmarks
- Open problems in NL2SQL (robustness, efficiency, real-world deployment)
- Comparison of Spider, BIRD, Spider 2.0 performance trajectories

## What It Does NOT Cover
- Systematic experimental comparison across dimensions
- Human-in-the-loop or reflection settings
- User prompt quality / intent ambiguity
- Schema cleanliness as a study axis

## Key Insights
- Spider is largely solved (>90% EX); BIRD remains challenging (~72–75% EX)
- Spider 2.0 exposes a new frontier with <30% success rates
- Open problems: schema-sparse settings, cost efficiency, auditability

## BibTeX
```bibtex
@article{luo2025nl2sqlsurvey,
  author    = {Yuyu Luo and Guoliang Li and Ju Fan and Chengliang Chai and Nan Tang},
  title     = {Natural Language to {SQL}: State of the Art and Open Problems},
  journal   = {Proceedings of the VLDB Endowment},
  volume    = {18},
  number    = {12},
  pages     = {5466--5471},
  year      = {2025},
  doi       = {10.14778/3750601.3750696}
}
```
