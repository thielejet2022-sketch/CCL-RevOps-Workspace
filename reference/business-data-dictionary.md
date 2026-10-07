# CCL Business & Data Dictionary

**Version:** 0.1  
**Updated:** 2026-10-07  
**Mode:** Candidate / pre-employment  
**Canonical source:** This GitHub file  
**Human-readable view:** Notion

## Purpose

Maintain governed CCL terminology across Marketing, Sales, Account Management, Delivery / Operations, Finance, systems, analytics, and the Signal Intelligence Engine.

This dictionary includes acronyms, roles, business concepts, lifecycle terms, data entities, systems, metrics, offerings, and other terminology whose meaning matters to Revenue Operations.

## Required fields

Every dictionary entry must include:

- **Term** — canonical term or acronym.
- **Category** — what kind of term it is.
- **Definition** — current evidence-backed meaning. Unknown portions stay explicit.
- **State** — evidence state using the same vocabulary as CCL workspace governance.
- **Source** — the evidence supporting the entry or the reason it remains unresolved.
- **Domain** — primary functional/business domain.
- **Notes / governance** — ambiguity, conflicts, validation needs, or usage rules.

### Evidence states

Use the canonical workspace states without creating a dictionary-specific substitute:

- **KNOWN** — supported by authoritative evidence such as a CCL system, document, policy, or otherwise reliable source.
- **REPORTED** — stated by a CCL stakeholder but not independently validated.
- **HYPOTHESIS** — plausible interpretation or belief that requires testing.
- **ASSUMPTION** — temporarily treated as true so work can proceed.
- **SYNTHETIC** — deliberately invented for prototypes, testing, or illustration.
- **UNKNOWN** — not yet available or unresolved.

**PROPOSED** remains a design-status label, not an evidence state.

### Categories

Use the smallest useful controlled vocabulary. Initial categories:

**Acronym · Role · Business Concept · Lifecycle / Process · Data Entity · System / Platform · Metric / KPI · Forecast / Finance · Offering · Organization / Function · Signal / Intelligence**

Add a category only when an existing category materially fails.

## Governance rules

1. GitHub is canonical. Notion is the human-readable reference view.
2. Every new term receives **Category + State + Source** when created.
3. Definitions must not exceed what the cited evidence supports.
4. If sources disagree, preserve the conflict in Notes rather than silently reconciling it.
5. A term may move between evidence states only when new evidence supports the change.
6. Candidate-era terms must not be promoted to current CCL operating truth without validation.
7. Canonical person/entity spelling follows `reference/canonical-entities.md`.
8. Material definition changes should remain explainable through Git history.
9. System fields, CRM stages, ownership rules, or metrics are not assumed merely because a business term exists.
10. Notion should reflect the current canonical GitHub definition, but GitHub governs in a conflict.

## Dictionary v0.1

| Term | Category | Definition | State | Source | Domain | Notes / governance |
|---|---|---|---|---|---|---|
| **CCL** | Acronym | Center for Creative Leadership. | KNOWN | CCL job description and stakeholder materials | Enterprise | Canonical organizational acronym. |
| **RevOps** | Acronym / Business Concept | Revenue Operations. In the CCL role context, a connective discipline spanning Marketing, Sales, Account Management, Operations / Delivery, Finance, systems, forecasting, analytics, and the client lifecycle. | KNOWN | Director, Revenue Operations job description | Enterprise | Do not reduce to CRM administration or Sales Operations. |
| **LSP** | Acronym / Role | Leadership Solutions Partner. Evidence shows a client-facing CCL role associated with faculty leadership and delivery; full formal scope across selling, design, delivery, and account management remains unresolved. | KNOWN | Bill Adam public LinkedIn role title supplied by JET; David Moore interview for delivery context | Delivery | Acronym expansion is known; full role boundaries are not. |
| **LSP Team Manager** | Role | Player/coach management role for Leadership Solutions Partners. Bill Adam's profile states responsibility for leading 7–8 LSPs, resourcing, people management, coaching, and mentoring. | KNOWN | Bill Adam public LinkedIn profile supplied by JET | Delivery | Enterprise reporting structure and resource-allocation authority remain UNKNOWN. |
| **Implementation Manager** | Role | Post-win operational/project-management role performing course information setup, participant registration, ordering, and behind-the-scenes execution support; David stated the role does not deliver instruction. | REPORTED | David Moore interview, 2026-10-06 | Delivery / Operations | Formal job definition and organizational placement require validation. |
| **Faculty** | Role / Organization / Function | People who design programs, run programs, and teach them; David described a hybrid model involving Leadership Solutions Partners and an adjunct pool. | REPORTED | David Moore interview, 2026-10-06 | Delivery | Relationship among Faculty, LSP, and design resources requires validation. |
| **Adjunct / Associate** | Role | Flexible delivery-resource pool used to navigate delivery capacity and seasonality; David reported more than 1,000 associates and adjuncts. | REPORTED | David Moore interview, 2026-10-06 | Delivery | Exact distinction between associate and adjunct is UNKNOWN. |
| **Closed Won** | Lifecycle / Process | Commercial contract/commitment point. Current evidence indicates this does not necessarily mean revenue has been delivered or recognized. | REPORTED | Demetreus Lancsweert interview, 2026-09-25; David Moore interview, 2026-10-06 | Sales / Finance / Delivery | Exact D365 stage definition and exit criteria are UNKNOWN. |
| **Scheduled Revenue** | Forecast / Finance | Future revenue associated with work that has been scheduled for delivery, providing greater visibility than unscheduled pipeline. | REPORTED | David Moore interview, 2026-10-06 | Finance / Delivery | Formal Finance definition, calculation, and system of record are UNKNOWN. |
| **Revenue Recognition** | Forecast / Finance | Financial recognition of revenue when applicable performance obligations are satisfied; timing differs by offering. | REPORTED | David Moore interview, 2026-10-06; Director, Revenue Operations job description | Finance | Finance remains authoritative for accounting policy. |
| **Open Enrollment** | Offering | CCL offering in which participants enroll in programs; David reported revenue is generally recognized after the program obligation is completed. | REPORTED | David Moore interview, 2026-10-06 | Commercial / Delivery / Finance | Formal product taxonomy requires validation. |
| **Custom Solution** | Offering | Client-specific leadership solution that may require design, scheduling, faculty/resources, and delivery before revenue recognition. | REPORTED | David Moore and Demetreus Lancsweert interviews | Commercial / Delivery / Finance | Exact CCL offering taxonomy requires validation. |
| **Account** | Data Entity | Commercial/client organization entity. Exact CCL definition, hierarchy, parent-child rules, and system boundaries are not yet established. | UNKNOWN | Account / Entity Discovery Framework; internal validation pending | Enterprise Data | Do not infer Dynamics cardinality or hierarchy. |
| **Opportunity** | Data Entity | Commercial pursuit/deal entity used in the sales process. Exact CCL field definition, stage model, and system behavior are not yet validated. | REPORTED | Demetreus Lancsweert interview; CCL uses Dynamics in stakeholder discussions | Sales / CRM | System configuration remains UNKNOWN. |
| **SIE** | Acronym / Signal / Intelligence | Signal Intelligence Engine: candidate-stage RevOps workstream for converting signals into account intelligence, prioritization, recommended action, human decision, outcomes, and learning. | PROPOSED | CCL RevOps Workspace design | RevOps / Analytics | PROPOSED is design status, not evidence state. This term is not asserted as current CCL terminology. |

## Validation queue

Priority terms whose definitions should be validated if JET joins CCL:

**Client · Customer · Account · Buying Organization · Opportunity · Lead · Qualified Lead · Pipeline · Booking / Bookings · Contracted Revenue · Scheduled Revenue · Recognized Revenue · Forecast · LSP · Faculty · Associate · Adjunct · Implementation Manager · Account Management · Customer Success · Program · Solution · Offering**

## Change pattern

When new evidence arrives:

**Evidence → identify term → assign Category → assign State → record Source → define only what evidence supports → record unknowns/conflicts → commit → update Notion reference view**

