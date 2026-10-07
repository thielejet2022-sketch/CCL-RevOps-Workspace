# CURRENT — CCL RevOps Workspace

**Updated:** 2026-10-07
**Mode:** Candidate / pre-employment
**Status:** ACTIVE

## Objective
Build a durable CCL Revenue Operations operating environment that can move from interview-stage hypothesis to validated operating system if JET joins CCL.

## Completed
- CCL GitHub repository created and connected.
- Initial governance architecture established.
- Candidate-mode evidence/hypothesis boundary established.
- Signal Intelligence Engine selected as first governed workstream.
- Initial SIE charter and signal schema scaffold created.
- Evidence-state vocabulary aligned between the ChatGPT Project and GitHub governance.
- ADR-0002 adopted: KNOWN / REPORTED / HYPOTHESIS / ASSUMPTION / SYNTHETIC / UNKNOWN, with PROPOSED retained separately as design status.

## Current workstream
**Signal Intelligence Engine (SIE)**

Goal: turn fragmented commercial signals across Sales, Marketing, Finance, customer/account activity, delivery/capacity, and other relevant CCL systems into governed intelligence that improves decisions, forecasting, prioritization, and intervention.

## Known context
Interview work has surfaced potential needs involving pipeline visibility, CRM usage consistency, forecasting, existing-account opportunity, commercial timing, capacity/utilization, and cross-functional RevOps alignment.

These remain **candidate-stage reported observations, hypotheses, assumptions, or unknowns** unless supported by authoritative CCL evidence and promoted to **KNOWN**.

## Next action
Define the **CCL Signal Taxonomy v0.1**:
- signal domains
- individual signal definitions
- source/system
- entity level
- trigger logic
- business meaning
- recommended action
- owner
- confidence/evidence status

Then test the taxonomy against 3–5 concrete CCL commercial scenarios.

## Blockers
- No direct access yet to CCL CRM/data architecture.
- Finance requirements remain substantially hypothesis-driven.
- Final CCL nomenclature and ownership model require validation.

## Open decisions
- Final SIE name and CCL-facing terminology.
- Whether delivery/capacity signals are a standalone domain or part of Finance/Operations.
- Minimum viable implementation layer after discovery: CRM-native, BI/data layer, or hybrid.

## Resume command
**GO CCL SIGNAL TAXONOMY**
