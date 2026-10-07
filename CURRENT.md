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
- CCL Signal Taxonomy v0.1 created with 7 domains and 21 candidate-stage signals.
- Signal schema v0.1 updated to align with governed evidence states and separate evidence state from design status.

## Current workstream
**Signal Intelligence Engine (SIE)**

Goal: turn fragmented commercial signals across Sales, Marketing, Finance, customer/account activity, delivery/capacity, data/process, and external conditions into governed intelligence that improves decisions, forecasting, prioritization, and intervention.

## Current design state
Signal Taxonomy v0.1 now includes:
- Sales / Pipeline
- Marketing / Demand
- Account / Expansion
- Finance / Commercial Timing
- Delivery / Capacity
- Data / Process
- External / Strategic

The taxonomy is deliberately implementation-neutral and contains no production thresholds.

## Next action
Test **CCL Signal Taxonomy v0.1** against five concrete commercial scenarios:

1. $900K scheduled program shifts across fiscal years.
2. Large strategic opportunity remains in pipeline but delivery lead time makes current-year recognition unlikely.
3. Region manages pipeline outside CRM, degrading forecast and attribution.
4. Marketing campaign produces lead volume but weak sales acceptance/conversion.
5. Existing account shows plausible expansion opportunity with no active pursuit.

For each scenario:
- identify signals that fire;
- trace evidence → interpretation → action;
- identify overlap/conflict;
- identify missing data;
- refine signal definitions;
- assess whether the recommendation is useful and explainable.

## Blockers
- No direct access yet to CCL CRM/data architecture.
- Production thresholds cannot be validated.
- Final CCL nomenclature, ownership model, and system-of-record boundaries require validation.

## Open decisions
- Final SIE name and CCL-facing terminology.
- Minimum viable implementation layer after scenario testing: CRM-native, BI/data layer, or hybrid.
- Whether Account/Expansion remains standalone after deeper client-lifecycle discovery.
- Which signals are MVP versus later-stage.

## Resume command
**GO TEST SIGNAL SCENARIOS**
