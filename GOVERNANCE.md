# Governance

## Source-of-truth model
GitHub is the governed source of truth for durable RevOps frameworks, definitions, schemas, decision records, and canonical project state. Notion may be used for narrative knowledge, interview preparation, research, stakeholder-facing working pages, and reference views.

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

## Candidate-mode boundary
Until JET is an authorized CCL employee with appropriate access, do not represent proposed designs as current CCL process; do not assume system fields, stages, integrations, ownership, metrics, or data quality; keep interview-derived information distinguishable from validated operating documentation; and avoid storing sensitive information that does not belong in this repository.

## Change discipline
Material changes to definitions, schemas, operating rules, or architecture should be explainable through commit history and, when useful, a decision record under `decisions/`.

## Session handoff
`CURRENT.md` is the canonical resume point. At the end of a meaningful work session, update Completed, Current workstream, Next action, Blockers, Open decisions, and Resume command. A future session should read `CURRENT.md` before continuing durable work.

## Design standard
Prefer: **Evidence → Signal → Interpretation → Decision → Action → Outcome → Learning**

The system should reduce ambiguity and decision latency, not merely create more dashboards.
