# CCL Signal Scenario Tests v0.1

**Status:** PROPOSED
**Stage:** Candidate / pre-employment
**Updated:** 2026-10-07

## Purpose
Pressure-test Signal Taxonomy v0.1 against five concrete CCL commercial situations before selecting production thresholds, systems, automation, analytics, or AI.

## Findings

### 1 — Scheduled program shifts across fiscal years
**Evidence:** REPORTED. Sarah described a large contract whose program timing moved from one fiscal year to another, materially changing CCL's fiscal-year picture while the client commitment remained.

**Signals:** Primary S-FIN-002 Scheduled Revenue Date Shift. S-MKT-002 may be affected if Marketing performance uses recognized-revenue timing. S-FIN-004 applies only if movement represents abnormal process delay.

**Decision:** Separate timing change from commercial loss. Reforecast realization, preserve the commercial commitment, capture the reschedule reason, and update affected functional views.

**Result:** KEEP S-FIN-002 distinct.

### 2 — Strategic opportunity can close, but current-year recognition is unlikely
**Evidence:** REPORTED. Demetreus described contract win as distinct from revenue and noted that late-year wins may have too little time to be scheduled and executed before fiscal year end. David separately described the gap between contract win and revenue recognition.

**Signals:** Primary S-FIN-003 Pipeline-to-Recognition Window Risk. S-PIP-003 applies only if pursuit quality is weak. After win, S-FIN-001 may apply if work remains unscheduled. S-DEL-001 applies if capacity blocks execution.

**Decision:** Separate booking forecast from revenue-realization forecast.

**Result:** KEEP S-FIN-003 separate from S-PIP-003. One asks whether CCL will win; the other asks when a win can become revenue.

### 3 — Region manages pipeline outside CRM
**Evidence:** REPORTED. Sarah described regional pipeline management in spreadsheets, with downstream impact on Marketing attribution, forecasting, and global consistency.

**Signals:** Primary S-DAT-001 CRM Adoption / Regional Process Exception. Secondary S-MKT-002 and S-DAT-002. S-PIP-001 may become unreliable because source completeness is compromised.

**Decision:** Treat this as a data-confidence exception with commercial consequences, not merely a user-adoption issue.

**Result:** REFINE S-DAT-001 so it can reduce confidence in downstream signals and forecasts.

### 4 — Marketing produces volume but weak sales acceptance/conversion
**Evidence:** REPORTED. Demetreus described multiple Marketing channels with source codes, weak downstream feedback, and inconsistent use of ICP criteria.

**Signals:** Primary S-MKT-001 Lead Quality / Sales Acceptance Gap. Secondary S-MKT-002. Conditional S-MKT-003. Portfolio-level S-MKT-004 if the pattern creates a net-new pipeline gap.

**Decision:** Diagnose the conversion break before changing spend or assigning fault. Test attribution completeness, ICP fit, Sales acceptance/follow-up, and downstream conversion in that order.

**Result:** KEEP the Marketing signals but enforce causal ordering.

### 5 — Existing account has plausible expansion opportunity but no active pursuit
**Evidence:** REPORTED. Sarah described trapped value in existing accounts and current identification of that value as subjective.

**Signals:** Primary S-ACC-001 Existing-Account Expansion Opportunity. S-ACC-002 does not inherently fire because whitespace and deteriorating engagement are different conditions.

**Decision:** Present an explainable expansion hypothesis to the human account owner rather than an opaque propensity score.

**Result:** KEEP S-ACC-001 but do not operationalize it until account hierarchy, purchase history, ownership, offering taxonomy, and expansion patterns are better understood.

## Cross-scenario conclusions
1. The seven-domain taxonomy survives the first pressure test.
2. Signal confidence must distinguish **data confidence** from **interpretation confidence**.
3. Signals need dependency rules. Example: CRM process exceptions can reduce confidence in pipeline coverage signals.
4. CCL needs separate **commercial/booking** and **revenue-realization** forecast lenses.
5. SIE should identify the break point before assigning functional fault.
6. Expansion intelligence should remain explainable and human-reviewed.

## MVP candidates
**Tier 1**
- S-FIN-002 Scheduled Revenue Date Shift
- S-FIN-003 Pipeline-to-Recognition Window Risk
- S-DAT-001 CRM Adoption / Regional Process Exception
- S-MKT-001 Lead Quality / Sales Acceptance Gap
- S-MKT-002 Campaign Attribution Feedback Gap

## Recommended v0.2 changes
1. Split confidence into data_confidence and interpretation_confidence.
2. Add signal dependency/qualification fields.
3. Add forecast_lens.
4. Add reason_code / causal classification.
5. Preserve all 21 signals for now; add no new signals until v0.2 architecture is applied.
6. Build the Account/Entity Model before expansion scoring.
7. Keep production thresholds unset until historical CCL data is available.

## Next step
Create Signal Taxonomy v0.2 with these architecture changes, then define the CCL Account/Entity Model v0.1.
