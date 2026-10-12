# Demand-quality diagnostic — synthetic test findings
Date: 2026-10-12
Mode: Candidate / pre-employment. All cases, events, timestamps and quantities below are SYNTHETIC. Design status: PROPOSED.
Instrument tested: [Demand-quality diagnostic](demand-quality-diagnostic-v0.1.md).
Method: manual scenario walkthrough and metric arithmetic. This is a design calibration, not independent stakeholder agreement, software validation or real CCL performance analysis.

## Result
Core diagnostic separates demand suitability from routing and execution. Five measurement ambiguities required refinement: lifecycle events versus current dispositions; record duplicates versus buying-event counts; unknown response compliance; no-decision win-rate treatment; and observed delay versus causal loss.
Verdict: suitable for further discovery after v0.2 refinements. Internal validity and stakeholder adoption remain untested.

## Completed case A — enrollment misrouted to custom sales
Case ID SYN-A. Proposed M1; first-time individual enrollment, employer reimbursement. Unit: one enrollment buying event, one participant, separate employer payer.
Day 0: eligible participant requests a specific program date. Synthetic program rules and seat availability establish fit. Same day: assigned to custom seller.
Day 2: seller marks reject, “not enterprise.” Day 3: reviewer identifies wrong route. Day 4: enrollment owner accepts transfer. Day 6: participant confirms enrollment.
Fit YES; readiness YES; routing initially NO then YES; execution compliance UNKNOWN because no response standard is supplied.
SPICED: individual development need and date supplied; enterprise budget committee unnecessary.
Initial seller judgment rejected; reviewer disposition reroute; current disposition accept. History retains reject → reroute → accept.
Primary diagnosis ROUTING, high scenario-evidence confidence. No evidence of bad fit. Funding by employer does not itself establish organizational buying motion.
Action: transfer with context and receiving confirmation. Endpoint observed: one enrollment, not a custom opportunity.
Timing: six days entry-to-enrollment; four days entry-to-receiving acceptance. Do not claim all four days were caused by misrouting.
Pass: correct route and measurement unit preserved; no duplicate new lead on transfer.

## Completed case B — custom demand with stalled follow-up
Case ID SYN-B. Proposed M3; new organization, one buying initiative; two contacts linked to it.
Day 0: L&D director requests help improving manager effectiveness for a rollout in 90 days; grants sponsor access. Desired outcome is stated but not quantified. Buying process, budget and delivery feasibility UNKNOWN.
Day 3: second contact submits same initiative. Day 5: seller labels demand “no response”; activity record shows no outreach. Day 7: owner contacts sponsor. Day 9: discovery validates organizational problem and desired impact; agreed next step is stakeholder meeting on day 14. No signed agreement or approved value at cutoff.
Fit YES on available scenario evidence; readiness YES for discovery, not proven ready to purchase; correct routing YES; initial follow-up not completed. SLA breach UNKNOWN without an agreed standard.
Seller rejection is unsupported by the supplied record. Reviewer: pending/unworked at day 5; accepted at day 7. Second form submission is linked to the original buying event.
Primary diagnosis EXECUTION; contributing DATA/discovery gaps. Do not conclude execution caused a lost sale.
SPICED: Situation/Pain available; Impact qualitative; Critical Event reported; Decision incomplete.
Action: owner-led discovery plus Delivery feasibility review before commitment. At cutoff: one validated problem-qualified opportunity under the synthetic gate, two contacts, zero bookings. Value remains UNKNOWN, not a fabricated pipeline amount.
Pass: no rejection for unknown budget; no duplicate opportunity; no financial value inferred.

## Adversarial variants
| Test | Synthetic evidence | Expected result | Walkthrough result |
|---|---|---|---|
| Low readiness | Target-account L&D researcher downloads paper and explicitly states no current initiative | Recycle with trigger; fit may be positive, readiness low | PASS; engagement not counted as buying intent |
| Missing outcome | No response or sale evidence accessible | Outcome UNKNOWN; disclose coverage | PASS; no conversion failure invented |
| Rejected but suitable | Seller says wrong lead; relevant problem and correct audience documented | Evidence review, distinguish judgment from truth | PASS; disagreement retained |
| Delivery constraint | Custom buyer ready, requested date explicitly infeasible under synthetic capacity evidence | Delivery/commercial reason; assess alternate date/scope | PASS; no Marketing fit failure implied |
| Trapped value | Dormant custom case returns with a new critical event; same original initiative resumes | Reactivation flag, retain original lineage; no fresh acquisition | PASS |
| Existing-account obstacle | Active pursuit needs proof for Finance stakeholder | Coordinated proof and agreed next step | PASS; progression is observed, content causality not established |
| True unsuitable demand | Documented mandatory eligibility criterion not met; no valid alternative route | Reject with fit reason and evidence | PASS; diagnostic does allow evidence-based rejection |
| Entitled service | Existing license holder requests included content | Enablement/service, not paid expansion | PASS |

## Metric arithmetic — deliberately synthetic, separate motions
### M1 cohort
Five distinct enrollment buying events, same entry window and equal observation time. Two rerouted; one eventually enrolls and one remains pending. Three never rerouted; two enroll and one remains recycled.
- Enrollment conversion: 3/5 = 60%.
- Current dispositions: accepted 3/5; pending 1/5; recycled 1/5. Sum 100%.
- Ever-rerouted events: 2/5 = 40%; current reroute count zero. These are different views.
- No reroute creates an additional denominator event.
- Three enrollments do not prove marketing incrementality or recognized revenue.
### M3 cohort
Six distinct initiative handoffs represented by eight source records; two records are duplicates of existing initiatives.
Fit assessed for four events: three fit and one unsuitable. Two unknown.
Response standard exists for four due events: two compliant, one verified breach, one missing activity evidence. Two other events lack an agreed standard.
Two of six events become qualified opportunities. One wins; the other remains open.
- Buying-event denominator six, not eight.
- Assessment coverage: 4/6 = 66.7%; confirmed fit among assessed: 3/4 = 75%; unknown 2/6.
- Qualified-opportunity conversion: 2/6 = 33.3%.
- Response tri-state for four eligible events: compliant 2/4 = 50%, noncompliant 1/4 = 25%, unknown 1/4 = 25%. Two without a standard separately disclosed.
- Compliance among assessed responses: 2/3 = 66.7%; response evidence coverage 3/4 = 75%. Never present 66.7% without coverage.
- Won/resolved: 1/1 = 100%; won/created-to-date: 1/2 = 50%; one open. Neither tiny-sample figure is a CCL benchmark.
- No portfolio conversion obtained by pooling M1 enrollment with M3 opportunity outcomes.
Arithmetic checked directly from scenario counts. Samples are not population estimates.

## Refinements applied to stable instrument path (v0.2)
1. Separate current disposition from event history and reroute incidence; exclude duplicate records from unique buying-event denominators while retaining duplicate-record data-quality reporting.
2. Split follow-up compliance into compliant/noncompliant/unknown and distinguish cases with no agreed standard.
3. Define resolved outcomes to include won, lost and closed/no-decision; report unresolved opportunities and alternative won/created view distinctly.
4. Introduce explicit UNRESOLVED primary diagnosis when evidence cannot select a cause. Mark cause versus correlation and confidence.
5. Retain stage-entry and disposition timestamps; measurement at cutoff is not the disposition at original handoff.

## Implications
Sarah's trapped-value hypothesis can be investigated through reactivation and stalled-case tests without overstating recoverable value.
Demetreus' lead concern can be investigated through motion-specific fit/readiness and actual downstream outcomes. Synthetic tests demonstrate that routing/execution can mimic poor quality; they do not establish these as CCL's actual causes.

## Next
Build a proposed joint Marketing–Sales calibration agenda using these cases, with definitions and evidence decisions to resolve before authorized internal review. Coordinate with existing GTM evidence request; do not create a competing data request.
Internal diagnosis requires authorized evidence and confirmed owners. No production scoring, threshold, D365 configuration or SIE taxonomy changed; no outreach sent.
