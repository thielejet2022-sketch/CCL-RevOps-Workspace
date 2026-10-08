# Bill Adams Interview → SIE Taxonomy v0.2 Reconciliation

**Date:** 2026-10-08
**Status:** PROPOSED evidence assessment, not an approved taxonomy revision
**Mode:** Candidate / pre-employment
**Canonical baseline:** [Signal Taxonomy v0.2](signal-taxonomy-v0.2.md), 7 domains / 21 signals
**Interview evidence:** Bill Adams, Director, Design & Delivery - Americas, October 8, 2026; [Pocket source](https://app.heypocket.com/app/share/bsFbypdt)
**Human-readable source:** [Notion evidence page](https://app.notion.com/p/3f3550a770198125aefde4527cfe0f22)

## Bottom line

Preserve all 21 existing signals. Bill's 13 candidate signals yield **8 direct extensions/mappings, 3 potential distinct additions, and 2 cross-domain compositions**. These counts are working classification, not approved architecture. None are production rules. The most important gap is **design-resource opportunity cost**, particularly Passport custom design consumption versus LSP availability for new pursuits.

## Reconciliation matrix

| # | Bill-derived candidate | Existing taxonomy anchor | Disposition | Rationale / validation |
|---|---|---|---|---|
| 1 | Pre-sale LSP assignment delay | S-DEL-001 Implementation Capacity Constraint; S-PIP-002 Stage Aging | **Potential new** pre-sale design-capacity signal | Existing S-DEL-001 is implementation/revenue-realization oriented; LSP assignment occurs before contract and affects booking. Confirm LSP assignment timestamp and stage gates. |
| 2 | Passport design estimate vs entitlement | S-DEL-001; S-DAT-002 Definition / Metric Inconsistency | **Potential new** scope/entitlement exception | No existing signal explicitly compares promised design services with contracted entitlement. Confirm Passport tiers, credits, included design hours, approvals. |
| 3 | Actual design effort burn vs plan | S-DEL-001 | **Extend** capacity signal | Resource load can be upstream of scheduling risk; requires time capture, planned hours and exception reasons. |
| 4 | Capacity displacement from Passport/custom rework | S-DEL-001; S-PIP-001 Pipeline Coverage Risk | **Potential new** capacity opportunity-cost signal | Crosses booking and realization lenses; differentiate from generic implementation capacity. Requires competing demand, skill constraints and prioritization authority. |
| 5 | Contract-to-IM handoff delay | S-DEL-002 Sales-to-Operations Handoff Incomplete; S-FIN-004 Contract-to-Cash Cycle Delay | **Extend** handoff | Named IM and handoff completeness are candidate attributes, not separate top-level signal yet. |
| 6 | Faculty/adjunct readiness gap | S-DEL-001 | **Extend** capacity | Resource qualification and readiness as subtypes; validate availability and qualifications data. |
| 7 | Client logistics readiness gap | S-DEL-002; S-DEL-001 | **Extend** handoff/capacity | Venue, materials, event producer and client dependencies can qualify readiness. |
| 8 | Delivery date/revenue timing movement | S-FIN-002 Scheduled Revenue Date Shift; S-FIN-003 Pipeline-to-Recognition Window Risk | **Extend** existing Tier 1 signal | Explicit reason codes for capacity/scope/client; do not equate schedule move with recognized revenue without Finance rules. |
| 9 | Expansion through new audience/business unit | S-ACC-001 Existing-Account Expansion Opportunity | **Extend** existing Tier 3 signal | Bill reports expansion across leadership levels and divisions. Requires hierarchy and offering history. |
| 10 | Repeat open-enrollment attendance | S-ACC-001; S-ACC-002 Account Engagement Deterioration | **Cross-domain composition** | Enrollment repetition is account/relationship evidence, not a validated standalone signal; open-enrollment ownership UNKNOWN. |
| 11 | Passport renewal + customization stress | S-ACC-002; S-DEL-001; S-ACC-001 | **Cross-domain composition** | Renewal economics and client relationship signal together; avoid inventing churn predictor. |
| 12 | Experiential value feedback gap | S-MKT-001 Lead Quality / Sales Acceptance Gap; S-MKT-002 Campaign Attribution Feedback Gap | **Extend** marketing evidence loop | Bill's marketing critique is a stakeholder hypothesis; test outcome evidence and message effectiveness before asserting causal gap. |
| 13 | Forecast vs resource readiness mismatch | S-FIN-001 Won-but-Unscheduled Revenue Risk; S-FIN-003; S-DEL-001; S-DAT-003 Required Forecast Evidence Missing | **Extend** existing dependency chain | Add resource feasibility as confidence context for distinct booking and realization forecasts. |

## Proposed taxonomy treatment (NOT APPROVED)

1. **Keep all existing IDs and 21 definitions intact.**
2. Candidate extension **S-DEL-001**: design/faculty/adjunct capacity subtypes, planned-vs-actual design hours, staffing conflicts; do not assume all pre-sale constraints fit a revenue-realization-only signal.
3. Candidate extension **S-DEL-002**: named IM, scoped handoff packet, client/venue/courseware readiness as evidence dimensions.
4. Candidate extension **S-FIN-002**: scope/design/resource as possible schedule-shift reason codes, pending actual data.
5. Candidate extension **S-ACC-001**: audience-level expansion, multi-business-unit whitespace, post-delivery feedback.
6. Candidate **new signal family** (IDs not assigned): pre-sale LSP availability, Passport entitlement/scope variance, and design-capacity opportunity cost. Evaluate whether to model as three independent event types or a common design-resource domain.
7. **Do not automatically count open-enrollment repeat attendance, Passport renewal stress, or experiential learning messaging as new production signals.** Test whether they are features, compositions, or playbook triggers.

## Bill's reported facts and limitations

- Custom client account team: Strategic Business Partner (Sales), LSP (design/faculty), and Implementation/Project Manager (Ops); IM enters after contract.
- Bill manages LSPs and assigns them to new sales pursuits; he reported a Passport customization example consuming **53 hours in two weeks** for one LSP. This is an anecdote, not an estimated norm.
- Bill described Passport tier credits/design time, scope tension, 18 North American LSPs, and over 100 adjunct faculty. All are **REPORTED**, not verified headcount or contract terms.
- Open enrollment is separate; its account ownership and relationship logic are UNKNOWN.
- D365 participation differs by function; do not infer object model, workflow automation or data completeness.
- Capacity/forecast approval committee exists according to Bill, but its formal name and authority are UNKNOWN.

## Decision Contract stress test (SYNTHETIC)

**Observation:** A qualified custom opportunity requests LSP design support; all suitable LSPs are allocated, including to Passport customization.
**Data confidence:** UNKNOWN until assignments, time and suitability can be verified.
**Interpretation confidence:** UNKNOWN; workload overlap alone does not prove lost revenue.
**Forecast lenses:** Booking exposure (pursuit support) and revenue-realization exposure (committed delivery) must be separately assessed.
**Human owner:** Candidate LSP manager + SBP + resource lead; validate decision rights.
**Recommendation:** Review entitlement/scope, available skills and alternative staffing before reprioritizing.
**Outcome:** Assignment completed, scope revised, opportunity delayed, or no impact, with reason captured.

## Validation queue

1. Verify SBP/LSP/IM role definitions, stage transitions, and decision rights with CCL process owners.
2. Retrieve Passport product/contract entitlement and design-service exception policies.
3. Inspect LSP/adjunct assignment and time tracking, forecast/capacity committee inputs.
4. Determine D365 versus delivery-system sources and their identifiers.
5. Review real historical exceptions and outcomes before approving new signal IDs or thresholds.
6. Validate open-enrollment client ownership and repeat-attendance linkage.
7. Validate Finance's revenue-recognition and forecast-period treatment.

## Governance decision

**No production taxonomy change.** This reconciliation is an evidence-gated proposal. Retain v0.2 and the CURRENT.md HOLD until authoritative CCL access or stakeholder validation permits revision.
