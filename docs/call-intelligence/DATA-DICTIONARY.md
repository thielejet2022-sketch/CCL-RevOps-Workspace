# Call Intelligence Data Dictionary v0.1 — PROPOSED

All IDs are stable strings; do not reuse. Date-times should include time zone where known. Empty means UNKNOWN, not false.

| Entity | Required fields | Additional fields |
|---|---|---|
| Meeting | meeting_id, date, purpose, source_locator, source_type | participants, consent_status, owner, confidentiality, source_version |
| Evidence | evidence_id, meeting_id, statement, evidence_class, source_pointer | speaker, topic, recorded_at, verification_status, sensitivity |
| Intelligence | intelligence_id, proposition, status, confidence, rationale | business_domain, alternative_explanation, impact, last_reviewed |
| EvidenceLink | intelligence_id, evidence_id, relationship | note; relationship = supports / challenges / contextualizes |
| Action | action_id, description, owner, status, origin_ref | due_date, priority, decision_required, outcome, closed_at |
| Stakeholder | stakeholder_id, role, functional_area | reporting_scope, source_reference, validation_status |
| DiscoveryQuestion | question_id, question, related_intelligence_id, status | intended_owner, priority, answer_evidence_id |

Evidence classes: KNOWN (directly validated), REPORTED (stakeholder statement), HYPOTHESIS (interpretation), ASSUMPTION (temporary premise), SYNTHETIC (test example), UNKNOWN (not established). HYPOTHESIS should ordinarily live in Intelligence, not Evidence.

Intelligence status: proposed, investigating, corroborated, challenged, validated, disproven, superseded. 'Corroborated' is multiple accounts, not system validation.

Confidence: low / medium / high, with stated rationale. Do not turn confidence into a fabricated numeric probability.

Action status: proposed, approved, in_progress, waiting, completed, canceled. An extracted suggestion is PROPOSED until authorized.

Privacy: stakeholder names and sensitive notes belong in approved restricted storage; public GitHub may contain field definitions but no personal record values.

Traceability: Meeting -> Evidence -> EvidenceLink -> Intelligence -> Action / DiscoveryQuestion -> Outcome. A claim without a source pointer is an unverified note, not evidence.
