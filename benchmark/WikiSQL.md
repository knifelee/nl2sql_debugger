# WikiSQL: Seq2SQL — Generating Structured Queries from Natural Language using Reinforcement Learning

## Paper

- **Title:** Seq2SQL: Generating Structured Queries from Natural Language using Reinforcement Learning
- **Authors:** Victor Zhong, Caiming Xiong, Richard Socher (Salesforce Research)
- **Venue:** arXiv 2017
- **ArXiv:** https://arxiv.org/abs/1709.00103
- **Dataset:** https://github.com/salesforce/WikiSQL

---

## Overview

WikiSQL was the first large-scale crowdsourced NL2SQL dataset and helped launch the modern era of NL2SQL research. It is built from Wikipedia tables and contains simple SQL queries with no joins.

---

## Dataset Statistics

| Property | Value |
|---|---|
| Total NL-SQL pairs | 80,654 |
| Tables | 24,241 |
| SQL structure | SELECT + WHERE only (no JOIN, GROUP BY, etc.) |
| Split | Train 56,355 / Dev 8,421 / Test 15,878 |

---

## SQL Grammar

WikiSQL SQL is restricted to:
```sql
SELECT [agg] col FROM table WHERE col op val [AND col op val ...]
```
- Aggregations: COUNT, SUM, AVG, MAX, MIN
- Operators: =, >, <, >=, <=, !=
- No joins, subqueries, GROUP BY, HAVING, ORDER BY

---

## Current State

WikiSQL is **largely solved** — top models achieve >90% execution accuracy. It is no longer used as a research frontier but remains useful as:
- A simple baseline evaluation
- A pre-training target for NL2SQL models
- A demonstration dataset for production systems

---

## Relevance to Ambiguity Research

WikiSQL's simplicity means **minimal structural ambiguity** — the SQL grammar is so constrained that most questions have unique valid SQL. It is not suitable for studying the types of ambiguity in AmbiQT or AMBROSIA. However, it provides:
- A **lower bound** or sanity check for new models
- Simple column/value linking challenges (value disambiguation)

---

## Citation

```bibtex
@article{zhong2017seq2sql,
  title = "Seq2SQL: Generating Structured Queries from Natural Language using Reinforcement Learning",
  author = "Zhong, Victor and Xiong, Caiming and Socher, Richard",
  journal = "arXiv preprint arXiv:1709.00103",
  year = "2017",
  url = "https://arxiv.org/abs/1709.00103"
}
```
