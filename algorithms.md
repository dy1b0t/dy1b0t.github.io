---
layout: default
title: Enhancement Two — Algorithms & Data Structures
permalink: /algorithms
---

# Enhancement Two — Algorithms & Data Structures

Introduced deterministic controls and safer ingestion loops for the event-scraping pipeline.

> **Formal submission available:** [Download Word document](./narratives/enhancement-two-algorithms-data-structures.docx)

## Summary
- Added index- and range-based URL selection for precise scraping windows
- Implemented deterministic parsing and validation to avoid ambiguous inputs
- Persisted run-state to support pause/resume/restart without container restarts

## Evidence of Improvement
- Scraping scope can be constrained to minimize cost and noisy data
- Deterministic inputs reduce unexpected branching and simplify testing
- Stateful control enables safer on-call operations and faster recovery

## Related Work
- [Software Engineering & Design](./software-engineering)
- [Databases](./databases)
