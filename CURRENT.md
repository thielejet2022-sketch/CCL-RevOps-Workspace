# CURRENT — CCL RevOps Workspace

**Updated:** 2026-10-07
**Mode:** Candidate / pre-employment
**Status:** ACTIVE

## Objective
Build a durable CCL Revenue Operations operating environment that can move from interview-stage hypothesis to validated operating system if JET joins CCL.

## Completed
- Governance architecture, evidence states, and canonical entity-name governance established.
- **Demetreus Lancsweert** established as canonical spelling.
- SIE selected as first governed workstream.
- Signal Taxonomy v0.1 created: 7 domains / 21 signals.
- Five commercial scenarios pressure-tested.
- Signal Schema v0.2 created.
- **Signal Taxonomy v0.2 created**, preserving all 21 signals while applying:
  - separate data confidence and interpretation confidence;
  - commercial/booking vs revenue-realization forecast lenses;
  - signal dependencies and confidence qualification;
  - causal ordering for Marketing and revenue realization;
  - reason-code support;
  - MVP tiering.
- No numeric production thresholds or implementation technology selected.

## Current workstream
**Signal Intelligence Engine (SIE)**

## Current architecture
Signals → Account Intelligence → Prioritization → Recommended Action → Human Decision → Outcome → Learning

Signal Taxonomy v0.2 now distinguishes:
- whether the source data can be trusted;
- whether the interpretation can be trusted;
- which forecast lens is affected;
- which upstream signals qualify the conclusion;
- what action is recommended;
- what remains unknown.

## MVP Tier 1
- S-FIN-002 Scheduled Revenue Date Shift
- S-FIN-003 Pipeline-to-Recognition Window Risk
- S-DAT-001 CRM Adoption / Regional Process Exception
- S-MKT-001 Lead Quality / Sales Acceptance Gap
- S-MKT-002 Campaign Attribution Feedback Gap

## Next action
Define **CCL Account/Entity Model v0.1** before attempting expansion scoring or richer account intelligence.

Model at minimum:
- organization/account hierarchy;
- people and buying roles;
- opportunity;
- contract;
- program/delivery;
- campaign/source;
- geography/region;
- offering;
- ownership;
- relationships across those entities.

The model must distinguish KNOWN/REPORTED structure from HYPOTHESIS/ASSUMPTION and must not invent Dynamics 365 object configuration.

## Blockers
- No direct access yet to CCL CRM/data architecture.
- Production thresholds cannot be validated.
- Final CCL nomenclature, ownership model, account hierarchy, and system-of-record boundaries require validation.

## Open decisions
- Final SIE name and CCL-facing terminology.
- Minimum viable implementation layer after model design: CRM-native, BI/data layer, or hybrid.
- Final MVP signal set after entity-model testing.
- CCL account hierarchy and entity-resolution rules.

## Resume command
**GO ACCOUNT ENTITY MODEL**
