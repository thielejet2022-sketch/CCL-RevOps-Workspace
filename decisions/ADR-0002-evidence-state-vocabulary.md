# ADR-0002 — Standardize Evidence-State Vocabulary

**Date:** 2026-10-07
**Status:** ACCEPTED

## Decision
Standardize CCL RevOps evidence states on:

- **KNOWN**
- **REPORTED**
- **HYPOTHESIS**
- **ASSUMPTION**
- **SYNTHETIC**
- **UNKNOWN**

Treat **PROPOSED** separately as a design-status label rather than an evidence state.

## Context
The ChatGPT Project instructions and the initial repository governance used overlapping but different vocabularies. The repository used VALIDATED, OBSERVED, HYPOTHESIS, PROPOSED, and UNKNOWN, while the Project instructions used KNOWN, REPORTED, HYPOTHESIS, ASSUMPTION, SYNTHETIC, and UNKNOWN.

Maintaining two vocabularies would create ambiguity when classifying interview evidence, candidate-stage assumptions, prototypes, and future-state designs.

## Rationale
The standardized model preserves the distinctions needed during candidate/pre-employment work:

- **KNOWN** separates authoritative evidence from stakeholder statements.
- **REPORTED** preserves stakeholder testimony without overstating certainty.
- **HYPOTHESIS** captures testable interpretation.
- **ASSUMPTION** allows work to proceed while explicitly carrying uncertainty.
- **SYNTHETIC** prevents prototype/test content from being mistaken for CCL data.
- **UNKNOWN** makes unresolved information visible.
- **PROPOSED** remains useful, but describes future-state design status rather than evidentiary certainty.

## Consequences
- GOVERNANCE.md uses the standardized vocabulary.
- New durable CCL artifacts should use these evidence states.
- Existing material using VALIDATED or OBSERVED should be translated when touched:
  - VALIDATED → KNOWN
  - OBSERVED stakeholder statement → REPORTED
  - OBSERVED directly verified evidence → KNOWN
- PROPOSED remains available as a separate design-status label.
