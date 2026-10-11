# SIE Qualification Framework — CCL Candidate Design

**Status:** HYPOTHESIS / PROPOSED DESIGN — NOT CCL APPROVED  
**Date:** 2026-10-10  
**Owner:** Candidate-stage RevOps design; business owners and validators not assigned.  
**Source:** JET's proposed three-layer qualification table (2026-10-10), refined with CCL stakeholder context. This is not a description of CCL's existing qualification policy.

## BLUF

Use **three independent decision dimensions**, not sequential gates or a single weighted lead score:

1. **Account Fit:** Is this organization strategically relevant to CCL?
2. **Solution Fit:** Is there a plausible, economically and operationally suitable CCL offering for this need?
3. **Pursuit Readiness:** Is there enough verified buying evidence to justify the next commercial investment?

Assess each independently, record **evidence, unknowns, confidence, owner, and next action**. An account may have high strategic fit and low pursuit readiness. A strong buyer signal cannot compensate for impossible delivery.

## Proposed criteria and decisions

| Dimension | Proposed evidence to inspect | Output / possible human decision | Main validation question |
|---|---|---|---|
| Account Fit | Organizational scale; leadership complexity; relevant business challenges; geographic alignment; long-term development potential; existing relationships | Strategic target / develop / monitor / deprioritize | Which attributes correlate with CCL's actual account outcomes? |
| Solution Fit | Use-case relevance; buyer profile; delivery requirements; economics; demand signals; purchasing model | Offering-specific fit assessment, including delivery and margin caveats | Which fit signals vary by Custom, Open Enrollment, Passport, coaching, or other offerings? |
| Pursuit Readiness | Identified economic buyer; urgency; funding; buying committee; competitive differentiation; delivery feasibility; mutual action plan | Pursue / develop / requalify / disengage | Which evidence predicts progression, wins and realizable delivery? |

**Important:** The original screenshot calls these “layers.” This design treats them as parallel dimensions for inspection, not a fixed sequence. The listed criteria are hypotheses, not approved CCL policy.

## Minimum assessment record (business model, not D365 fields)

- **Entity and scope:** account; optional specific opportunity; offering family; assessment date
- **Dimension:** Account Fit, Solution Fit or Pursuit Readiness
- **Evidence:** observation or signal; source; observed date; person responsible for validation
- **Status:** supported / mixed / unsupported / insufficient evidence (proposed labels)
- **Confidence:** high / medium / low / unknown, with reason (not numerical)
- **Why it matters:** impact on commercial decision, revenue timing, or delivery feasibility
- **Unknown / dependency:** unanswered question, required evidence, owner
- **Recommended action:** named next step with rationale and human decision maker
- **Outcome:** decision taken, subsequent result, and date for learning

This is a conceptual record specification, **not** a request to add fields or automate workflow in Dynamics 365.

## Decision logic before scoring

- **Account Fit strong + Solution Fit weak:** research alternative offerings; do not force a deal.
- **Account Fit strong + Solution Fit strong + Readiness weak:** nurture or develop buying evidence; do not equate potential with forecast.
- **Fit weak + Readiness strong:** inspect mismatch, delivery and economics; urgency alone is insufficient.
- **Delivery feasibility uncertain:** flag a cross-functional review with Sales, Design & Delivery, Operations, and Finance as relevant.
- **Evidence stale, missing or conflicting:** mark **insufficient evidence**; ask for validation rather than inventing certainty.
- **Existing client expansion:** evaluate at the account **and** offering/opportunity level; avoid assuming a single account score explains every motion.

These are illustrative **proposed** decision patterns, not rules adopted by CCL.

## Offering-specific considerations (hypotheses)

- **Custom solutions:** client need, account-team coverage, LSP/design capacity, implementation, scheduling, economics.
- **Open Enrollment:** participant demand, cohort availability, enrollment timing, and recognition timing.
- **Passport:** license/entitlement fit, utilization, design-time demand, renewal/expansion potential.
- **Coaching:** buyer and participant fit, coach availability, engagement structure.

Bill Adams reported custom account team roles, Passport design-capacity tension and a cross-functional capacity review. David Moore reported distinctions between contracted, scheduled and recognized revenue. **Neither interview establishes the proposed qualification model or its weights.**

## Validation plan

1. **Discovery:** interview Sales, Marketing, Design & Delivery, Operations and Finance to learn actual qualification decisions, handoffs, terminology and existing sources.
2. **Data audit:** identify source systems and whether historical account/opportunity, offering, delivery and financial outcomes can be joined reliably.
3. **Retrospective test:** review a diverse sample of won, lost, stalled, renewed and expanded cases. Avoid survivorship bias. Record which proposed criteria were knowable **at the time of decision**.
4. **Decision trial:** apply the three dimensions manually in a small set of live or synthetic cases, recording decisions and follow-up outcomes.
5. **Refinement:** retire weak criteria; revise definitions; consider weights only if evidence, sample size, governance and explainability justify them.
6. **Operationalization checkpoint:** obtain business-owner and Finance approval before changes to D365, policy, score or automation.

**Candidate validation metrics:** usefulness to human decision makers; completeness and freshness of evidence; qualification-to-next-stage progression; win/loss and no-decision patterns; delivery feasibility; forecast timing; expansion and renewal outcomes. Metrics are candidate tests, not established CCL KPIs.

## Separation of governed artifacts

- **Business & Data Dictionary:** term definitions and evidence states, including existing **Account Fit** entry.
- **SIE Qualification Framework (this file):** criteria, decision dimensions, evidence expectations, and test design.
- **Signal Dictionary (future/parallel):** precisely defined observable events, provenance, recency, and owners.
- **D365:** operational source/system configuration only after discovery and approval.

## Open decisions / risks

- Are these the right three dimensions for CCL's distinct offering families?
- Is Pursuit Readiness best evaluated at opportunity level, rather than account level?
- How are economic buyer, buying committee and delivery feasibility defined and owned?
- Which historical outcomes are reliable enough for validation?
- Do qualification judgments require region-specific adaptation?
- Do not mistake high confidence in an opinion for strong source evidence.

**Next:** Build a compact, human-reviewable assessment template and pressure-test it against two contrasting **synthetic** CCL scenarios before using any real CCL account data.
