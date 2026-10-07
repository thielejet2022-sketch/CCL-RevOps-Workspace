# Signal Schema v0.1

**Status:** PROPOSED
**Stage:** Candidate / pre-employment

| Field | Purpose |
|---|---|
| signal_id | Durable unique identifier |
| signal_name | Human-readable signal name |
| domain | Sales/Pipeline, Marketing/Demand, Account/Expansion, Finance/Timing, Delivery/Capacity, Data/Process, External/Strategic, etc. |
| evidence_state | KNOWN, REPORTED, HYPOTHESIS, ASSUMPTION, SYNTHETIC, UNKNOWN |
| design_status | PROPOSED, APPROVED, IMPLEMENTED, RETIRED |
| evidence_basis | Source, stakeholder, document, or system supporting the signal concept |
| source_system | Originating system or source |
| source_object | Account, opportunity, campaign, program, invoice, engagement, etc. |
| entity_level | Account, opportunity, campaign, program, region, seller, client, etc. |
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

Evidence state and design status are separate:
- evidence state describes how strongly the underlying assertion is supported;
- design status describes whether the signal definition itself is proposed, approved, implemented, or retired.

## Next design task
Test the CCL Signal Taxonomy v0.1 against concrete commercial scenarios before choosing implementation technology.
