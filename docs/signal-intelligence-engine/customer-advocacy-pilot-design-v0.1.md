# Customer Advocacy Pilot Design v0.1
Date: 2026-10-11
Mode: Offer Accepted / Pre-Start
State: HYPOTHESIS / PROTOTYPE ONLY. No live CCL workflow, taxonomy or CRM change authorized.
Canonical context: CURRENT.md; SIE taxonomy v0.2 stays 7 domains / 21 signals.

## BLUF
Design a 30-day human-reviewed research pilot for three public examples: HOYA Vision Care, First Citizens Bank, loanDepot. This is a design horizon, not a scheduled CCL deployment. Test whether attributable public praise can lead to defensible account-level recommendations; never equate public praise with referral consent.

## Test cases
HOYA: customer-reported measurable program impact; validate measure, attribution and rights to reuse.
First Citizens: multi-year program endorsement and awards; validate relationship continuity and permissions.
loanDepot: corporate announcement plus participant testimonials; validate individual and corporate permissions independently.
Sources and evidence states: customer-advocacy-validation-2026-10-11.md.

## Decision contract and gates
1. OBSERVE: source URL, date, author, employer, exact claim, program, provenance; failed verification => HOLD.
2. INVESTIGATE: match account/program/contact using authorized internal systems; check current relationship, sensitive issues, account owner and contractual restrictions; unknown => NO OUTREACH.
3. RECOMMEND: human owner reviews specific proposal (thank-you, case study request, reference invitation, introduction inquiry, expansion discovery, or no action), its evidence and uncertainty; no automatic recommendation.
4. PERMISSION: record specific, explicit consent for any reuse, quote, reference or introduction; permission for one use does not imply permission for others.
5. LEARN: record owner decision, approved outreach, permission granted/declined, reference participation, introductions, meetings, qualified opportunities, revenue outcomes; distinguish sourced versus influenced and avoid unsupported causality.

## Minimum pilot record (research worksheet, NOT production schema)
case_id; account_candidate; post_url; observed_at; source_author; source_type; claim_summary; reported_outcome; evidence_confidence; interpretation_confidence; account_match_status; owner_status; permission_status; proposed_action; human_decision; decision_reason; action_date; result; follow_up; notes.
Use UNKNOWN rather than blank or guessed values; never store unnecessary personal data.

## Pilot schedule (proposed)
Week 1: verify sources, fill evidence worksheet and unresolved questions.
Week 2: role-play human review with SYNTHETIC owner and permission states; no customer outreach.
Week 3: pressure-test decision contract with three different advocacy types and edge cases.
Week 4: assess signal utility, false positives, missing information, permission gates and recommendation clarity. Decide retain/refine/defer.

## Evaluation criteria (no numerical score or threshold)
Evidence traceable? Account identification unambiguous? Confidence and uncertainty explicit? Does recommendation change a human decision? Is owner clear? Permission respected? Can action/outcome be captured without conflating reference, referral and expansion? Which gaps block real-world use?

## Roles (hypothetical, not CCL assignments)
Analyst/researcher: captures source and evidence.
Account owner: validates relationship and makes action decision.
Customer advocacy/marketing or legal reviewer: validates reuse and consent policy where required.
RevOps: ensures definitions, handoffs and learning measures.
All actual ownership UNKNOWN pending discovery.

## Guardrails
No CRM fields, scoring weights, thresholds, automation, customer contact, implied consent, account hierarchy claims or taxonomy additions. Use synthetic data for role-play and label it SYNTHETIC.

## Open discovery questions
Who owns references? Are advocacy permissions centrally governed? What qualifies a reference vs referral? Which account hierarchy governs global clients? How are program outcomes verified? How are sourced vs influenced opportunities defined? What does D365 currently capture?

## Next
Create a three-case research worksheet and conduct a synthetic decision-review simulation. Resume: GO CCL ADVOCACY SIMULATION.
