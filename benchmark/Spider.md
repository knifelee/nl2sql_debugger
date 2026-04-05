# Spider: A Large-Scale Human-Labeled Dataset for Complex and Cross-Domain Semantic Parsing and Text-to-SQL Task

## Paper

- **Title:** Spider: A Large-Scale Human-Labeled Dataset for Complex and Cross-Domain Semantic Parsing and Text-to-SQL Task
- **Authors:** Tao Yu, Rui Zhang, Kai Yang, Michihiro Yasunaga, Dongxu Wang, Zifan Li, James Ma, Irene Li, Qingning Yao, Shanelle Roman, Zilin Zhang, Dragomir Radev
- **Venue:** EMNLP 2018
- **ArXiv:** https://arxiv.org/abs/1809.08887
- **Dataset site:** https://yale-lily.github.io/spider
- **Leaderboard:** https://yale-lily.github.io/spider

---

## Overview

Spider is the **de facto standard benchmark** for cross-domain, complex NL2SQL. It requires models to generalize to unseen databases and produce complex SQL involving JOINs, GROUP BY, HAVING, subqueries, and set operations.

---

## Dataset Statistics

| Property | Value |
|---|---|
| Total NL-SQL pairs | 10,181 |
| Databases | 200 |
| Domains | 138 |
| Avg SQL complexity | Complex (multi-join, nested) |
| Split | Train 7K / Dev 1K / Test (hidden) |

## SQL Difficulty Levels

| Level | Description |
|---|---|
| Easy | Simple SELECT, no JOIN |
| Medium | Single JOIN or simple aggregation |
| Hard | Multiple JOINs, GROUP BY, HAVING |
| Extra Hard | Nested queries, set operations |

---

## Limitations (Relevant to Ambiguity Research)

- Single ground-truth SQL per question — ignores inherent ambiguity
- Crowdsourced questions may not reflect real user intent distribution
- No multi-turn or clarification capability
- Many "ambiguous" questions silently assigned one interpretation by annotators

These limitations directly motivated AmbiQT, AMBROSIA, and PRACTIQ.

---

## Evaluation Metrics

- **Exact Match (EM):** Whether predicted SQL exactly matches gold SQL (after normalization)
- **Execution Accuracy (EX):** Whether predicted SQL returns the same results as gold SQL

---

## Citation

```bibtex
@inproceedings{yu-etal-2018-spider,
  title = "Spider: A Large-Scale Human-Labeled Dataset for Complex and Cross-Domain Semantic Parsing and Text-to-{SQL} Task",
  author = "Yu, Tao and Zhang, Rui and Yang, Kai and others",
  booktitle = "Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing",
  year = "2018",
  url = "https://arxiv.org/abs/1809.08887"
}
```

---

## Variants and Extensions

- **Spider-DK:** Domain knowledge required
- **Spider-Syn:** Synonym-based question paraphrase robustness
- **Spider-Realistic:** More realistic questions without explicit schema element mentions
- **Spider-HJ:** Modified to require more complex joins (from HLR-SQL paper)
- **Spider 2.0:** Updated version with more complex real-world schemas (2024)
