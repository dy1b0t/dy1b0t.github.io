---
layout: default
title: Enhancement Three — Databases
permalink: /databases
---

# Enhancement Three — Databases

Strengthened data integrity and cost efficiency in the ingestion flow.

> **Formal submission available:** [Download Word document](./narratives/enhancement-three-databases.docx)

## Summary
- Added pre-validation to detect duplicates before expensive processing
- Integrated checks that cut AI token usage by rejecting known duplicates early
- Ensured consistency across PostgreSQL and MongoDB storage paths

## Evidence of Improvement
- Reduced redundant writes and API spend
- Higher data quality with fewer conflicting records
- Clearer ingestion lineage across both data stores

## Related Work
- [Software Engineering & Design](./software-engineering)
- [Algorithms & Data Structures](./algorithms)
