# CCL Signal Taxonomy v0.2

**Status:** PROPOSED
**Stage:** Candidate / pre-employment
**Updated:** 2026-10-07
**Supersedes:** Signal Taxonomy v0.1 for active design work

## Purpose
Apply the architecture findings from scenario testing to CCL's 21-signal taxonomy without inventing production thresholds or system mappings.

## Core architecture
Every signal now distinguishes:
- **Evidence state:** how strongly the underlying assertion is supported.
- **Data confidence:** whether source data is sufficiently complete, timely, and governed.
- **Interpretation confidence:** whether the observed condition reliably means what the signal says it means.
- **Forecast lens:** commercial/booking, revenue realization, both, or N/A.
- **Dependencies:** upstream signals that qualify, suppress, or contextualize the signal.
- **Reason code:** causal classification where known.

At candidate stage, confidence values and reason-code enumerations remain **UNKNOWN / TO VALIDATE** unless directly supported.

## Domain 1 — Sales / Pipeline

### S-PIP-001 — Pipeline Coverage Risk
- Evidence state: KNOWN + REPORTED
- Forecast lens: Commercial/booking; may inform revenue realization only after timing logic is applied
- Trigger: Qualified pipeline for a defined period falls below the validated coverage required to achieve target.
- Data confidence dependency: S-DAT-001 and S-DAT-002 can reduce confidence.
- Interpretation: Future target attainment may be at risk before the miss appears in recognized revenue.
- Action: Diagnose by source, segment, stage, seller, and expected realization period.
- Validation: Coverage ratios, segmentation, horizon, CRM completeness.

### S-PIP-002 — Stage Aging / Stalled Opportunity
- Evidence state: KNOWN + REPORTED
- Forecast lens: Commercial/booking
- Trigger: Opportunity remains in stage beyond validated norm or lacks required progression evidence.
- Data confidence dependency: S-DAT-001.
- Interpretation: Close probability or timing may be overstated.
- Action: Validate next step, buyer engagement, decision criteria, close date, and stage.
- Validation: Stage benchmarks and exit criteria.

### S-PIP-003 — Large-Deal Conversion Risk
- Evidence state: REPORTED
- Forecast lens: Commercial/booking
- Evidence basis: Demetreus reported more $1M+ pursuits while win rate was declining.
- Trigger: Strategic opportunity shows validated characteristics associated with conversion risk.
- Interpretation: Concentrated pipeline value may exaggerate attainable bookings.
- Action: Executive deal review covering buying committee, value case, competition, and pursuit strategy.
- Validation: Strategic-deal threshold and loss-pattern features.

### S-PIP-004 — Close-Date Credibility Risk
- Evidence state: REPORTED
- Forecast lens: Commercial/booking; may affect revenue realization downstream
- Trigger: Close date is repeatedly moved or lacks validated buyer evidence.
- Dependencies: S-DAT-003 may contextualize missing forecast evidence.
- Interpretation: Forecast-period placement may be unreliable.
- Action: Revalidate close date using buyer-confirmed milestones and historical timing.
- Validation: Push-count and evidence standards.

## Domain 2 — Marketing / Demand

### S-MKT-001 — Lead Quality / Sales Acceptance Gap
- Evidence state: KNOWN + REPORTED
- Forecast lens: Commercial/booking
- Trigger: Qualified demand shows materially weak sales acceptance or downstream conversion.
- Dependencies: Evaluate S-MKT-002 and S-MKT-003 before assigning cause.
- Interpretation: Demand volume may not be translating into commercially useful opportunities.
- Action: Diagnose attribution, ICP fit, qualification, rejection reasons, SLA adherence, and follow-up.
- Validation: Lifecycle definitions and acceptance benchmarks.

### S-MKT-002 — Campaign Attribution Feedback Gap
- Evidence state: REPORTED
- Forecast lens: N/A
- Trigger: Marketing activity cannot be reliably connected to downstream pipeline, revenue, or loss outcome.
- Dependencies: S-DAT-001 and S-DAT-002 may be root causes.
- Interpretation: Marketing investment decisions lack closed-loop evidence.
- Action: Resolve attribution path, source-code integrity, campaign association, and outcome capture.
- Validation: Attribution model and completeness standard.

### S-MKT-003 — ICP Fit Exception
- Evidence state: REPORTED
- Forecast lens: Commercial/booking
- Evidence basis: Demetreus reported that CCL has an ICP definition but does not consistently use it as a strict driver.
- Trigger: Prospect materially falls outside validated ICP criteria but enters active pursuit.
- Interpretation: Commercial capacity may be diverted toward lower-probability or lower-value demand.
- Action: Confirm strategic exception or route/disqualify.
- Validation: ICP fields, thresholds, and exception policy.

### S-MKT-004 — New-Logo Generation Weakness
- Evidence state: REPORTED
- Forecast lens: Commercial/booking
- Trigger: New-logo qualified pipeline creation or conversion falls below plan or validated benchmark.
- Dependencies: S-MKT-001, S-MKT-002, S-MKT-003 may explain the break point.
- Interpretation: Existing-account performance may mask insufficient future net-new growth.
- Action: Diagnose source, ICP segment, region, rep, campaign, and conversion step.
- Validation: Net-new definition and benchmarks.

## Domain 3 — Account / Expansion

### S-ACC-001 — Existing-Account Expansion Opportunity
- Evidence state: REPORTED
- Forecast lens: Commercial/booking
- Trigger: Existing client matches a validated expansion pattern but lacks active pursuit.
- Interpretation: Commercial whitespace may exist inside the installed client base.
- Action: Produce an explainable expansion hypothesis with evidence, missing information, confidence, and recommended human review.
- Validation: Account hierarchy, offering history, buying centers, ownership, and expansion patterns.
- Design constraint: No opaque propensity score before the Account/Entity Model is validated.

### S-ACC-002 — Account Engagement Deterioration
- Evidence state: HYPOTHESIS
- Forecast lens: N/A until relationship between engagement and commercial outcomes is validated
- Trigger: Meaningful engagement falls below validated account/segment benchmark.
- Interpretation: Relationship health, expansion, renewal, or delivery risk may be changing.
- Action: Human account-health review.
- Validation: Engagement telemetry and outcome relationship.

## Domain 4 — Finance / Commercial Timing

### S-FIN-001 — Won-but-Unscheduled Revenue Risk
- Evidence state: REPORTED
- Forecast lens: Revenue realization
- Evidence basis: David and Demetreus described a gap between contract win and delivery/recognition.
- Trigger: Won work lacks an executable delivery/program date or sits outside expected realization window.
- Dependencies: S-DEL-001 and S-DEL-002 may provide causal context.
- Interpretation: Booking value may not translate into revenue in the assumed period.
- Action: Confirm delivery plan, client commitment, dependencies, and likely recognition period.
- Validation: Contract-to-schedule workflow and timing ranges.

### S-FIN-002 — Scheduled Revenue Date Shift
- Evidence state: REPORTED
- Forecast lens: Revenue realization
- Trigger: Scheduled delivery moves enough to change fiscal-period recognition.
- Interpretation: Revenue timing changes even though commercial commitment may remain intact.
- Action: Reforecast realization, preserve booking status, capture reason code, and update affected functional views.
- Candidate reason codes: Client reschedule, CCL capacity, delivery dependency, scope/design change, other/unknown.
- Validation: Materiality threshold, authoritative schedule source, reason-code taxonomy.

### S-FIN-003 — Pipeline-to-Recognition Window Risk
- Evidence state: REPORTED
- Forecast lens: Both, with distinct outputs
- Evidence basis: Demetreus reported that late-year wins may have too little time to be scheduled and executed before year end.
- Trigger: Expected close date plus expected post-sale delivery lead time extends beyond target recognition period.
- Dependencies: S-PIP-004 can alter commercial timing confidence; S-DEL-001 can alter realization timing.
- Interpretation: Opportunity may remain valid commercial pipeline while being unavailable to solve the current-period revenue gap.
- Action: Preserve booking forecast while shifting revenue-realization expectation.
- Validation: Lead-time distributions by offering/geography.

### S-FIN-004 — Contract-to-Cash Cycle Delay
- Evidence state: REPORTED
- Forecast lens: Revenue realization
- Evidence basis: David and Demetreus described the long path from prospect to contract to design/delivery to invoice/cash.
- Trigger: A major interval in contract → schedule → delivery → invoice → cash exceeds validated norm or commitment.
- Dependencies: S-DEL-001 and S-DEL-002 may identify upstream cause.
- Interpretation: Revenue/cash timing or operational execution may require intervention.
- Action: Identify stalled handoff/dependency and assign recovery action.
- Validation: Timestamps, SLA expectations, and authoritative system boundaries.

## Domain 5 — Delivery / Capacity

### S-DEL-001 — Implementation Capacity Constraint
- Evidence state: REPORTED
- Forecast lens: Revenue realization
- Trigger: Scheduled/expected implementation workload exceeds validated capacity.
- Affected signals: S-FIN-001, S-FIN-002, S-FIN-003, S-FIN-004.
- Interpretation: Won or scheduled work may be delayed.
- Action: Rebalance resources, prioritize, add flexible capacity, or adjust schedule.
- Validation: Capacity unit, workload model, planning horizon.

### S-DEL-002 — Sales-to-Operations Handoff Incomplete
- Evidence state: KNOWN
- Forecast lens: Revenue realization
- Trigger: Required post-sale data/documents are missing, inconsistent, or late.
- Affected signals: S-FIN-001 and S-FIN-004.
- Interpretation: Delivery setup and downstream timing may be delayed or error-prone.
- Action: Complete missing handoff elements and identify root cause.
- Validation: Handoff checklist and SLA.

## Domain 6 — Data / Process

### S-DAT-001 — CRM Adoption / Regional Process Exception
- Evidence state: REPORTED
- Forecast lens: N/A; confidence modifier
- Trigger: Required CRM activity, opportunity, stage, or forecast data falls below validated completeness/timeliness standard.
- Affected signals: S-PIP-001, S-PIP-002, S-PIP-004, S-MKT-002, S-MKT-004 and any other CRM-dependent signal.
- Interpretation: Commercial conclusions may be directionally useful but less trustworthy.
- Action: Quantify missing coverage, reconcile off-system pipeline, identify workflow/system friction, and remediate.
- Validation: Required fields, usage, timeliness, regional exceptions.
- Design rule: This signal can reduce **data_confidence** without changing **interpretation_confidence**.

### S-DAT-002 — Definition / Metric Inconsistency
- Evidence state: KNOWN + REPORTED
- Forecast lens: N/A; confidence modifier
- Trigger: Functions/reports calculate or label the same commercial concept differently.
- Affected signals: Any signal using the disputed definition.
- Interpretation: Apparent performance differences may be definitional rather than operational.
- Action: Govern business definition, calculation logic, authoritative source, and retirement of conflicting versions.
- Validation: Governance authority and metric catalog.

### S-DAT-003 — Required Forecast Evidence Missing
- Evidence state: HYPOTHESIS
- Forecast lens: Commercial/booking
- Trigger: Opportunity is forecast without validated evidence required for that category.
- Affected signals: S-PIP-004 and forecast aggregation.
- Interpretation: Forecast confidence may exceed actual deal evidence.
- Action: Obtain evidence or downgrade classification.
- Validation: Forecast categories and evidence requirements.

## Domain 7 — External / Strategic

### S-EXT-001 — Macroeconomic Demand Risk
- Evidence state: REPORTED
- Forecast lens: Both, only after empirical relationship is validated
- Trigger: Validated external indicators deteriorate for exposed sectors/geographies and historically precede CCL commercial weakness.
- Interpretation: Demand or timing may weaken before internal lagging indicators reveal it.
- Action: Reassess assumptions, exposure, messaging, pipeline generation, and account risk.
- Validation: Indicator set, lag relationships, materiality.

### S-EXT-002 — Geopolitical / Travel Disruption Risk
- Evidence state: REPORTED
- Forecast lens: Revenue realization; commercial/booking where applicable
- Trigger: External event affects travel feasibility, client availability, geography, or delivery conditions for active/scheduled work.
- Affected signals: S-FIN-001, S-FIN-002, S-FIN-003 as applicable.
- Interpretation: Delivery/recognition may move even when demand remains intact.
- Action: Identify exposed programs/accounts, contingency options, and forecast timing impact.
- Validation: Exposure data and response playbook.

# Causal ordering

## Marketing diagnostic chain
S-MKT-002 Attribution completeness
→ S-MKT-003 ICP fit
→ S-MKT-001 Sales acceptance / lead quality
→ downstream opportunity conversion
→ S-MKT-004 portfolio-level new-logo weakness

The chain is diagnostic, not automatically causal. It prevents premature attribution of fault.

## Revenue-realization chain
Commercial opportunity
→ booking/contract
→ S-FIN-001 scheduling risk
→ S-DEL-002 handoff quality
→ S-DEL-001 capacity
→ S-FIN-002 schedule movement
→ delivery / recognition
→ S-FIN-004 contract-to-cash timing

## Data-confidence overlay
S-DAT-001 and S-DAT-002 can qualify downstream signal confidence. A low-confidence source should not silently produce a high-precision recommendation.

# MVP tiers

## Tier 1 — first validation candidates
- S-FIN-002 Scheduled Revenue Date Shift
- S-FIN-003 Pipeline-to-Recognition Window Risk
- S-DAT-001 CRM Adoption / Regional Process Exception
- S-MKT-001 Lead Quality / Sales Acceptance Gap
- S-MKT-002 Campaign Attribution Feedback Gap

## Tier 2 — requires stronger definitions/baselines
- S-PIP-001 through S-PIP-004
- S-MKT-003 and S-MKT-004
- S-FIN-001 and S-FIN-004
- S-DEL-001 and S-DEL-002
- S-DAT-002 and S-DAT-003

## Tier 3 — richer entity/data model required
- S-ACC-001 and S-ACC-002
- S-EXT-001 and S-EXT-002

# v0.2 design decisions
1. Preserve all 21 signals. No new signals added.
2. Separate commercial/booking forecast from revenue-realization forecast.
3. Split data confidence from interpretation confidence.
4. Allow data/process signals to qualify downstream confidence.
5. Add explicit signal dependencies and causal ordering.
6. Preserve human decision points, especially for expansion intelligence.
7. Do not assign numeric thresholds or confidence values until CCL evidence supports them.
8. Do not select implementation technology yet.

# Next step
Define **CCL Account/Entity Model v0.1**: organization/account hierarchy, people/buying roles, opportunity, contract, program/delivery, campaign/source, geography/region, offering, ownership, and the relationships required to connect signals across the client lifecycle.
