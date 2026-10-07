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
- Signal Taxonomy v0.1 created and five commercial scenarios pressure-tested.
- Signal Schema v0.2 created.
- Signal Taxonomy v0.2 created: 7 domains / 21 signals with confidence separation, forecast lenses, dependencies, causal ordering, reason-code support, and MVP tiering.
- Account/Entity modeling checkpoint completed: insufficient evidence exists to responsibly define CCL's actual domain model.
- **CCL Account / Entity Discovery Framework v0.1 created** to define what must be learned before building the Account/Entity Model.
- Actual Account/Entity Model intentionally deferred until evidence-led CCL lifecycle walkthroughs can validate terminology, entities, cardinalities, ownership, and system boundaries.

## Current workstream
**Signal Intelligence Engine (SIE) — Domain Discovery**

## Current architecture
Signals → Account Intelligence → Prioritization → Recommended Action → Human Decision → Outcome → Learning

The SIE signal layer is sufficiently developed for candidate-stage work. The next constraint is domain knowledge, not additional signal invention.

## Discovery framework
The framework covers:
- organization/account;
- people/stakeholders;
- opportunity/pipeline;
- contract/commercial commitment;
- delivery/program;
- offering/line of business;
- marketing source/campaign;
- geography/region;
- ownership;
- revenue/financial realization.

All unvalidated relationship cardinalities remain **UNKNOWN**.

## Recommended validation approach
When internal access is available, trace representative real examples end-to-end:
1. New-logo pursuit: Marketing → opportunity → contract → delivery → recognized revenue.
2. Existing-client expansion.
3. Global/complex client hierarchy.
4. Contract/program shifted across fiscal periods.
5. Representative examples from materially different lines of business.

Capture terminology, IDs, systems of record, ownership, relationships, timestamps, exceptions, manual work, and reporting consequences.

## Gate for Account/Entity Model v0.1
Do not build the actual model until core lifecycle entities, major cardinalities, authoritative systems, offering differences, hierarchy/ownership rules, and booking-to-revenue linkage have been validated.

## Next action
**Pause Account/Entity Model construction at the discovery gate.**

Candidate-stage SIE architecture is now approaching the point where additional detail would create assumptions faster than evidence.

Recommended next work should either:
- identify another evidence-supported candidate-stage SIE question worth resolving; or
- preserve this state and use the Discovery Framework as an early Day-0/transition artifact if JET joins CCL.

## Blockers
- Actual Account/Entity Model requires internal CCL domain evidence.
- No direct access yet to CRM/data architecture.
- Production thresholds cannot be validated.
- Final CCL nomenclature, ownership model, account hierarchy, and system-of-record boundaries require validation.

## Open decisions
- Final SIE name and CCL-facing terminology.
- Minimum viable implementation layer after internal discovery: CRM-native, BI/data layer, or hybrid.
- Final MVP signal set after entity-model validation.
- CCL account hierarchy and entity-resolution rules.

## Resume command
**GO DISCOVERY REVIEW**
