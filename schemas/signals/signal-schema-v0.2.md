# Signal Schema v0.2

**Status:** PROPOSED
**Stage:** Candidate / pre-employment
**Updated:** 2026-10-07

| Field | Purpose |
|---|---|
| signal_id | Durable unique identifier |
| signal_name | Human-readable signal name |
| domain | Governed signal domain |
| evidence_state | KNOWN, REPORTED, HYPOTHESIS, ASSUMPTION, SYNTHETIC, UNKNOWN |
| design_status | PROPOSED, APPROVED, IMPLEMENTED, RETIRED |
| evidence_basis | Source supporting the signal concept |
| source_system | Originating system or source |
| source_object | Source business object |
| entity_level | Entity affected by the signal |
| entity_id | Entity identifier |
| observed_at | When the condition was observed |
| trigger_definition | Rule or condition creating the signal |
| signal_value | Observed value or condition |
| business_meaning | Why the signal matters |
| data_confidence | Confidence that source data is complete, timely, and governed |
| interpretation_confidence | Confidence that the condition has the stated business meaning |
| severity | Relative urgency or importance |
| forecast_lens | Commercial/booking, revenue realization, both, or not applicable |
| reason_code | Governed causal classification where known |
| upstream_signal_ids | Signals that qualify, suppress, or contextualize this signal |
| affected_signal_ids | Downstream signals whose confidence or interpretation may change |
| recommended_action | Default intervention or investigation |
| action_owner | Function/person accountable for response |
| action_due | Expected response window |
| status | New, acknowledged, investigating, actioned, resolved, dismissed |
| outcome | Result of intervention |
| feedback | What was learned and whether the signal remains useful |

## Design notes
Evidence state describes support for the underlying assertion. Design status describes lifecycle state of the signal definition.

Scenario testing showed that source-data quality and interpretation quality are different. A pipeline signal can be logically sound while relying on incomplete CRM data.

Signals may qualify downstream signals. Example: a CRM adoption/process exception may reduce data confidence in a pipeline coverage signal.

CCL scenario testing also indicates that commercial/booking probability and revenue-realization probability must remain distinguishable.

## Implementation boundary
This schema remains implementation-neutral. It does not assume Dynamics 365 fields, a BI platform, warehouse model, workflow technology, AI model, or production thresholds.
