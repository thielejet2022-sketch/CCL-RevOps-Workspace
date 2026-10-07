# SIE Decision Contract v0.1

**Status:** PROPOSED
**Stage:** Candidate / pre-employment
**Updated:** 2026-10-07
**Scope:** CCL SIE candidate-stage governance
**Purpose:** Define the minimum information required for a detected signal to become actionable intelligence presented for human decision.

## Principle
A signal is not yet intelligence.

A detected condition becomes actionable intelligence only when SIE can explain:
1. what changed;
2. why it matters;
3. what evidence supports the conclusion;
4. how trustworthy the data is;
5. how trustworthy the interpretation is;
6. what important information is missing;
7. what action is recommended;
8. who should decide or act;
9. what happened after the decision.

The contract governs the **decision interface**, not the technology used to generate it.

## Decision Contract

### 1. Signal
**Question:** What changed?

Required:
- signal_id
- signal_name
- observed_at
- affected entity or scope
- observed condition/value
- trigger definition or reason the condition was surfaced

Rule: The output must describe the observed condition without overstating cause.

### 2. Business meaning
**Question:** Why does this matter?

Required:
- business_meaning
- affected commercial lens: commercial/booking, revenue realization, both, or N/A
- severity/priority where a validated method exists
- affected downstream signals or business outcomes where known

Rule: Distinguish an observed fact from an inferred consequence.

### 3. Evidence
**Question:** What supports the conclusion?

Required:
- evidence_state: KNOWN / REPORTED / HYPOTHESIS / ASSUMPTION / SYNTHETIC / UNKNOWN
- evidence_basis
- source system/source object when available
- relevant upstream signals
- reason code where supported

Rule: Evidence provenance must remain inspectable. SIE must not convert stakeholder report, hypothesis, assumption, or synthetic test data into fact.

### 4. Data confidence
**Question:** Can we trust the inputs?

Required:
- data_confidence
- known completeness/timeliness/governance issues
- material data/process signals affecting confidence
- source-of-record status when known

Rule: Low or unknown data confidence must be visible and must qualify downstream precision.

Candidate-stage constraint: Numeric confidence thresholds are not defined.

### 5. Interpretation confidence
**Question:** Can we trust what we think the data means?

Required:
- interpretation_confidence
- alternative plausible explanations where material
- dependencies or assumptions supporting the interpretation

Rule: Data can be accurate while interpretation remains uncertain. Do not collapse these confidence dimensions.

Candidate-stage constraint: Numeric confidence thresholds are not defined.

### 6. Missing information
**Question:** What do we still need to know?

Required when material:
- missing evidence
- unresolved assumptions
- validation needed
- whether missing information should block action, lower confidence, or merely be noted

Rule: SIE should surface uncertainty rather than manufacture completeness.

### 7. Recommended action
**Question:** Given the evidence, what should CCL do next?

Required:
- recommended_action
- rationale connecting evidence to action
- urgency/action_due when supported
- whether action is investigative, corrective, preventive, or opportunistic

Rule: Recommendations must be proportional to evidence and confidence. Weak evidence may justify investigation, not intervention.

### 8. Human decision and ownership
**Question:** Who owns the judgment?

Required:
- action_owner or decision owner
- decision/status
- human override/dismissal capability
- rationale for material overrides where operationally appropriate

Rule: SIE recommends. Humans retain accountable commercial judgment unless a later governed process explicitly authorizes automation.

### 9. Outcome and learning
**Question:** What happened?

Required after action where observable:
- outcome
- feedback
- resolution/status
- whether the signal/recommendation was useful
- evidence relevant to future threshold, rule, or model refinement

Rule: No SIE feedback loop exists unless outcomes are captured. Action without outcome capture produces activity, not learning.

## Minimum presentation standard
A human-facing SIE recommendation should be able to render this compact decision packet:

**WHAT CHANGED**
The observed signal and affected entity/scope.

**WHY IT MATTERS**
Business impact and forecast/commercial lens.

**EVIDENCE**
Supporting facts/reports plus provenance.

**CONFIDENCE**
Data confidence and interpretation confidence, shown separately.

**MISSING**
Material unknowns or assumptions.

**RECOMMENDED ACTION**
Specific next action and rationale.

**OWNER**
Human/function responsible for judgment or action.

**OUTCOME**
Captured after action to close the learning loop.

## Decision readiness states

### OBSERVE
Condition detected, but evidence/context is insufficient for a recommendation.
Default action: monitor or gather information.

### INVESTIGATE
Signal has enough relevance to warrant human investigation, but not enough support for a corrective/opportunistic action.
Default action: resolve missing evidence or causal ambiguity.

### RECOMMEND
Evidence and confidence support a specific human-reviewed action.
Default action: route recommendation to accountable owner.

### LEARN
Decision/action occurred and outcome evidence is available.
Default action: capture result and update signal usefulness, thresholds, or reasoning.

These are **PROPOSED decision-readiness states**, not current CCL workflow stages.

## Suppression / qualification rules
SIE should not present false precision.

A recommendation should be downgraded from RECOMMEND to INVESTIGATE or OBSERVE when:
- a material upstream data-confidence signal is unresolved;
- required evidence is missing;
- competing explanations materially change the recommended action;
- entity identity or ownership is unresolved;
- the trigger threshold itself is not validated and the action would be consequential.

A low-risk information-gathering action may still be recommended under uncertainty.

## Example: Scheduled Revenue Date Shift

**Signal:** S-FIN-002 Scheduled Revenue Date Shift.

**What changed:** A scheduled delivery date moved enough to alter fiscal-period revenue realization.

**Why it matters:** Revenue timing may move even though the commercial commitment remains intact.

**Evidence:** Delivery schedule plus finance forecast linkage. At candidate stage, authoritative systems remain UNKNOWN.

**Data confidence:** Depends on authoritative schedule source and reliable linkage to the financial forecast.

**Interpretation confidence:** Depends on whether the schedule movement actually changes recognition timing for the relevant offering.

**Missing:** Materiality threshold, reason-code taxonomy, authoritative systems, offering-specific recognition rules.

**Recommended action:** Reforecast realization, preserve commercial booking status unless separate evidence says otherwise, capture the reason for movement, and identify affected functional views.

**Owner:** Finance + Operations + RevOps, subject to validation of actual CCL ownership.

**Outcome:** Capture whether revenue moved as expected and whether the reason recurred.

**Readiness:** INVESTIGATE in candidate stage. It cannot be promoted to a production RECOMMEND rule until internal evidence validates the missing elements.

## Relationship to Signal Schema v0.2
Signal Schema v0.2 defines the information SIE can store about a signal.

The Decision Contract defines the minimum reasoning and presentation standard required before that signal should influence human action.

Schema answers: **What fields exist?**

Decision Contract answers: **What must be understandable before we act?**

## Technology boundary
This contract is implementation-neutral.

It does not assume:
- Dynamics 365 implementation;
- Power BI or another BI platform;
- a warehouse/lakehouse;
- Python;
- rules engine;
- machine-learning model;
- generative AI;
- workflow automation.

Any future implementation should satisfy the Decision Contract regardless of technology.

## Candidate-stage gate
This contract completes the candidate-stage conceptual SIE architecture.

Further CCL-specific work should require new evidence unless it is explicitly labeled as a generic/SYNTHETIC prototype.

Do not proceed to:
- production thresholds;
- scoring weights;
- account/entity cardinalities;
- automated recommendations;
- implementation architecture;
- AI/ML design

without the evidence required by the existing discovery gates.

## Resume condition
Resume CCL-specific SIE architecture when one or more of the following becomes available:
- JET joins CCL and gains internal discovery access;
- authoritative CCL process/system documentation becomes available;
- representative CRM/contract/delivery/finance data can be inspected;
- stakeholders validate previously UNKNOWN domain relationships or operating rules.

Until then, preserve the architecture as candidate-stage work.
