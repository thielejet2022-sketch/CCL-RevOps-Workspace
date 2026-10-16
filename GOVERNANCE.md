# Governance

## Source-of-truth model
GitHub is the governed source of truth for durable RevOps frameworks, definitions, schemas, decision records, canonical entity names, and canonical project state. Notion may be used for narrative knowledge, interview preparation, research, stakeholder-facing working pages, and reference views.

## Canonical names and entity identity
Names of CCL stakeholders and other durable entities must use the canonical spelling in `reference/canonical-entities.md`.

When source material, transcripts, filenames, meeting notes, speech-to-text, or other imported material conflicts with the canonical entity record:
- preserve the source text when quoting or retaining the original artifact;
- use the canonical spelling in analysis, summaries, schemas, decisions, handoffs, and new durable artifacts;
- do not normalize the canonical spelling to a more common variant;
- treat conflicting source labels as source metadata errors unless later authoritative evidence changes the canonical record.

For the current workspace, **Demetreus Lancsweert** is canonical. The variant **Demetrius** must not be used in newly authored CCL material.

## Evidence states
Every material CCL-specific assertion should be identifiable as:
- **KNOWN** — supported by authoritative evidence such as a CCL system, document, policy, or otherwise reliable source.
- **REPORTED** — stated by a CCL stakeholder but not yet independently validated.
- **HYPOTHESIS** — plausible interpretation or belief that requires testing.
- **ASSUMPTION** — not yet validated, but temporarily treated as true so work can proceed.
- **SYNTHETIC** — deliberately invented data, examples, scenarios, or structures used for prototypes, testing, or illustration.
- **UNKNOWN** — information that is not yet available or remains unresolved.

Do not silently promote a hypothesis, assumption, reported statement, or synthetic example into known fact.

### Design status
**PROPOSED** is a design-status label, not an evidence state. Use it for recommended future-state processes, schemas, operating models, fields, workflows, automations, metrics, or architecture that have not been approved or implemented.

A proposed design may also rely on assumptions or hypotheses. Keep those evidence states explicit.

## Operating modes and pre-start boundary
**Current: Offer Accepted / Pre-Start Mode**, effective 2026-10-16. JET confirmed acceptance on 2026-10-15 and a scheduled start of 2026-10-26. These are JET-confirmed milestones; they do not establish employment commencement, internal access, delegated authority or CCL adoption of these designs.

Use three distinct phases:
1. **Candidate / Pre-Employment** — historical research and interview preparation.
2. **Offer Accepted / Pre-Start** — current onboarding preparation, expectation alignment, learning and proposed 90-day planning.
3. **Employee / Operating** — enter after JET confirms employment has begun; confirm authority, authorized access and information-handling rules before operational execution.

Do not represent proposed designs as current CCL process or assume fields, stages, integrations, ownership, metrics or data quality. Preserve interview-derived provenance and SYNTHETIC labels. Acceptance does not validate operating assumptions or lift SIE HOLD.

This repository is public as verified on 2026-10-16. Keep internal, confidential and personal CCL information out unless CCL-approved handling and an appropriate destination are established. Do not infer storage approval from employment or technical access.

On transition, classify inherited material as **VALIDATED / PARTIALLY VALIDATED / DISPROVEN / STILL UNKNOWN / OBSOLETE**. These are review dispositions, separate from evidence states and design status. Record scope, evidence, date and the next validation step. See the [transition review](docs/offer-accepted-pre-start-transition-2026-10-16.md).

Dated decisions and historical checkpoints retain their original context; current mode is governed here and in CURRENT.md. Proposed signal/motion/framework candidates are not employment-status labels.

## Change discipline
Material changes to definitions, schemas, operating rules, entity identity, or architecture should be explainable through commit history and, when useful, a decision record under `decisions/`.

## Session handoff
`CURRENT.md` is the canonical resume point. At the end of a meaningful work session, update Completed, Current workstream, Next action, Blockers, Open decisions, and Resume command. A future session should read `CURRENT.md` before continuing durable work.

## Design standard
Prefer: **Evidence → Signal → Interpretation → Decision → Action → Outcome → Learning**

The system should reduce ambiguity and decision latency, not merely create more dashboards.

## JET's call preparation
For **BUILD CALL PREP — [person or meeting] — [date/time]**, follow [Call Prep Standard](docs/call-prep-standard.md) and [blank template](templates/call-prep-sheet.md). This is JET's private preparation workflow. Use current source records and preserve evidence/date/attribution boundaries. TEST ONLY creates no live appointment or delivery-log entry. Default output is a concise sheet in ChatGPT; PDF only on request. Private personal details remain in Airtable. Repository instructions do not automatically modify ChatGPT Project settings.
