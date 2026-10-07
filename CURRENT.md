# CURRENT — CCL RevOps Workspace

**Updated:** 2026-10-07
**Mode:** Candidate / pre-employment
**Status:** ACTIVE

## Objective
Build a durable CCL Revenue Operations operating environment that can move from interview-stage hypothesis to validated operating system if JET joins CCL.

## Completed
- CCL GitHub repository created and connected.
- Governance architecture and candidate-mode evidence boundary established.
- Evidence-state vocabulary aligned; ADR-0002 adopted.
- Canonical entity-name governance added; **Demetreus Lancsweert** is the canonical spelling.
- Signal Intelligence Engine selected as first governed workstream.
- CCL Signal Taxonomy v0.1 created with 7 domains and 21 candidate-stage signals.
- Five concrete commercial scenarios tested against Signal Taxonomy v0.1.
- Scenario testing validated the 7-domain structure and identified architecture refinements.
- Signal Schema v0.2 created with separate data/interpretation confidence, signal dependencies, forecast lens, and reason-code support.
- Existing Signal Taxonomy v0.1 corrected to use the canonical spelling **Demetreus**.

## Current workstream
**Signal Intelligence Engine (SIE)**

## Scenario-test conclusions
1. Commercial/booking probability and revenue-realization timing must remain separate forecast lenses.
2. Data/process exceptions can reduce confidence in downstream commercial signals.
3. Signal confidence must distinguish data confidence from interpretation confidence.
4. Marketing signals should diagnose the conversion break before assigning functional fault.
5. Expansion recommendations should remain explainable hypotheses until the account/entity model and supporting data are validated.
6. No v0.1 signal was removed.

## MVP candidates
Tier 1:
- S-FIN-002 Scheduled Revenue Date Shift
- S-FIN-003 Pipeline-to-Recognition Window Risk
- S-DAT-001 CRM Adoption / Regional Process Exception
- S-MKT-001 Lead Quality / Sales Acceptance Gap
- S-MKT-002 Campaign Attribution Feedback Gap

## Next action
Apply the scenario-test findings to create **Signal Taxonomy v0.2**, then define the **CCL Account/Entity Model v0.1** before attempting expansion scoring or richer account intelligence.

## Blockers
- No direct access yet to CCL CRM/data architecture.
- Production thresholds cannot be validated.
- Final CCL nomenclature, ownership model, and system-of-record boundaries require validation.

## Open decisions
- Final SIE name and CCL-facing terminology.
- Minimum viable implementation layer after model design: CRM-native, BI/data layer, or hybrid.
- Final MVP signal set after v0.2 taxonomy refinement.
- CCL account hierarchy and entity-resolution rules.

## Resume command
**GO SIGNAL TAXONOMY V0.2**
