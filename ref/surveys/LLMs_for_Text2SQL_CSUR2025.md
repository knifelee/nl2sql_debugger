---
title: "A Survey on Employing Large Language Models for Text-to-SQL Tasks"
venue: ACM Computing Surveys 2025
doi: https://dl.acm.org/doi/10.1145/3737873
arXiv: https://arxiv.org/abs/2407.15186
---

## Authors
Liang Shi, Xinyi Liu, Zhebin Zhu, Feifei Li, et al.

## Overview
A comprehensive survey focusing specifically on how LLMs are applied to Text-to-SQL tasks. Organizes methods into a three-stage pipeline: Pre-Processing, Inference, and Post-Processing. Covers both prompt engineering and fine-tuning approaches with practical insights for each subcategory.

## Dimensions Studied
- Pre-processing: schema linking, question understanding, context compression
- Inference: in-context learning, chain-of-thought, decomposition, agents
- Post-processing: self-correction, execution-guided refinement, re-ranking
- Fine-tuning: supervised, RLHF, domain adaptation

## What It Does NOT Cover
- Human-in-the-loop reflection types as a primary axis
- User prompt quality (good vs ambiguous)
- Schema cleanliness as a systematic study variable
- IR-level clarification approaches
- Data lake or schema-sparse settings

## Key Insights
- Post-processing (self-correction) is now a standard component of top systems
- Agent-based approaches dominate on complex benchmarks (Spider 2.0)
- Fine-tuning still competitive for narrow-domain deployment
- Schema linking remains the dominant bottleneck

## Relevance to Proposed Survey
This paper covers the post-processing/reflection stage at a high level but does not distinguish between LLM reflection vs human reflection vs IR-level reflection. The proposed survey would add systematic experimental comparison across these reflection types, which this survey leaves unstudied.

## BibTeX
```bibtex
@article{shi2025llmtext2sql,
  author    = {Liang Shi and Xinyi Liu and Zhebin Zhu and Feifei Li and others},
  title     = {A Survey on Employing Large Language Models for Text-to-{SQL} Tasks},
  journal   = {ACM Computing Surveys},
  year      = {2025},
  doi       = {10.1145/3737873},
  url       = {https://arxiv.org/abs/2407.15186}
}
```
