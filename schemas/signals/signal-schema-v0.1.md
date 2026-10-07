# Signal Schema v0.1

**Status:** PROPOSED
**Stage:** Candidate / pre-employment

| Field | Purpose |
|---|---|
| signal_id | Durable unique identifier |
| signal_name | Human-readable signal name |
| domain | Sales, Marketing, Finance, Account, Delivery/Capacity, Data/Process, etc. |
| evidence_state | VALIDATED, OBSERVED, HYPOTHESIS, PROPOSED, UNKNOWN |
| source_system | Originating system or source |
| source_object | Account, opportunity, campaign, program, invoice, engagement, etc. |
| entity_id | Entity affected by the signal |
| observed_at | When the triggering condition was observed |
| trigger_definition | Rule or condition that creates the signal |
| signal_value | Observed value or condition |
| business_meaning | Why the signal matters |
| confidence | Confidence in interpretation |
| severity | Relative urgency/importance |
| recommended_action | Default intervention or investigation |
| action_owner | Function/person accountable for response |
| action_due | Expected response window |
| status | New, acknowledged, investigating, actioned, resolved, dismissed |
| outcome | Result of the intervention |
| feedback | What was learned and whether the signal remains useful |

## Design note
The schema is intentionally implementation-neutral. It should not yet assume Dynamics 365 fields, a BI platform, a warehouse model, or workflow technology.

## Next design task
Populate this schema with a CCL Signal Taxonomy v0.1 and test it against concrete scenarios before choosing implementation technology.
