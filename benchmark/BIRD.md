# BIRD: A Big Bench for Large-Scale Database Grounded Text-to-SQLs

## Paper

- **Title:** Can LLM Already Serve as A Database Interface? A BIg Bench for Large-Scale Database Grounded Text-to-SQLs
- **Authors:** Jinyang Li, Binyuan Hui, Ge Qu, Jiaxi Yang, Binhua Li, Bowen Li, Bailin Wang, Bowen Qin, Rongyu Cao, Ruiying Geng, Nan Huo, Xuanhe Zhou, Chenhao Ma, Guoliang Li, Kevin C.C. Chang, Fei Huang, Reynold Cheng, Yongbin Li
- **Venue:** NeurIPS 2023 Datasets & Benchmarks Track (**Spotlight**)
- **ArXiv:** https://arxiv.org/abs/2305.03111
- **Benchmark site:** https://bird-bench.github.io/
- **Leaderboard:** https://bird-bench.github.io/

---

## Overview

BIRD (BIg bench for laRge-scale Database grounded text-to-SQL) is the most challenging widely-used NL2SQL benchmark as of 2024. It was motivated by the observation that **Spider is largely solved** (>90% accuracy by top models) but real-world NL2SQL remains far from solved.

Key innovations over Spider:
- **Real-world databases** with actual data (noisy, messy, complex)
- **External knowledge (evidence)** annotations: domain knowledge needed to understand queries
- **Much larger data volumes**: up to 33.4 GB of database content
- **Database value ambiguity**: query answers depend on actual data in the DB

---

## Dataset Statistics

| Property | Value |
|---|---|
| Total NL-SQL pairs | 12,751 |
| Databases | 95 |
| Domains | 37 |
| DB content size | 33.4 GB total |
| Evidence annotations | Yes (external knowledge) |
| Split | Train 9,428 / Dev 1,534 / Test (hidden) |

---

## Key Features Relevant to Ambiguity

1. **Database value ambiguity:** Queries depend on actual values in the database, not just schema
2. **Evidence annotations:** Require incorporating external domain knowledge (e.g., "account balance > 0 means in credit")
3. **Dirty data:** Real-world databases have NULL values, inconsistent formatting, etc.
4. **Noisy schema names:** Table/column names are often cryptic, abbreviated, or domain-specific

---

## Evaluation Metric: Execution Accuracy (EX)

BIRD uses execution accuracy as the primary metric (whether the result set matches), since exact SQL match is too strict for real-world complex queries. Also includes:
- **Valid Efficiency Score (VES):** Rewards SQL that is both correct and efficient

---

## Relationship to Ambiguity Research

BIRD exposes a type of ambiguity not well-captured by Spider: **value-level ambiguity** where the correct SQL interpretation depends on what values are actually present in the database. This is distinct from schema-induced ambiguity (AmbiQT) and linguistic ambiguity (AMBROSIA), but equally important in real deployment.

---

## Citation

```bibtex
@inproceedings{li2023bird,
  title = "Can LLM Already Serve as A Database Interface? A BIg Bench for Large-Scale Database Grounded Text-to-SQLs",
  author = "Li, Jinyang and Hui, Binyuan and Qu, Ge and others",
  booktitle = "Advances in Neural Information Processing Systems (NeurIPS)",
  year = "2023",
  url = "https://arxiv.org/abs/2305.03111"
}
```

---

## State-of-the-Art Results (as of early 2025)

| Model | Dev EX | Test EX |
|---|---|---|
| Human performance | ~92% | ~92% |
| Best LLM-based systems | ~72-75% | ~70-73% |
| GPT-4 (DIN-SQL) | ~55-60% | — |

The large gap between human and machine performance on BIRD (vs. near-closure on Spider) demonstrates that real-world NL2SQL remains unsolved.
