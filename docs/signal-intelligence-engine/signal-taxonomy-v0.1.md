# CCL Signal Taxonomy v0.1

**Status:** PROPOSED
**Stage:** Candidate / pre-employment
**Updated:** 2026-10-07

## Purpose
Define the first governed set of commercial and operational signal concepts for CCL's Signal Intelligence Engine (SIE).

This taxonomy is deliberately implementation-neutral. It does not assume final CRM fields, data architecture, automation platform, ownership model, or production thresholds.

## Evidence discipline
Signal concepts below are classified using the governed evidence model:

- **KNOWN** — supported by authoritative evidence such as a CCL document or system.
- **REPORTED** — stated by a CCL stakeholder but not independently validated.
- **HYPOTHESIS** — plausible interpretation requiring testing.
- **ASSUMPTION** — temporarily treated as true so design work can proceed.
- **SYNTHETIC** — invented for prototyping or testing.
- **UNKNOWN** — unresolved.

**PROPOSED** describes the design status of this taxonomy and is not an evidence state.

## Candidate-stage evidence base
The taxonomy is grounded primarily in:
- CCL Director, Revenue Operations job description.
- Sarah Nabors interview, 2026-09-04.
- Demetreus Lancsweert interview, 2026-09-25.
- David Moore interview, 2026-10-06.

Stakeholder statements are treated as **REPORTED** unless independently supported by authoritative documentation or systems.

---

## Domain 1 — Sales / Pipeline

### S-PIP-001 — Pipeline Coverage Risk
- **Evidence state:** KNOWN + REPORTED
- **Evidence basis:** Job description assigns pipeline governance and forward-looking pipeline risk; stakeholders described need for stronger pipeline visibility and conversion.
- **Candidate source/system:** CRM + forecast model
- **Entity level:** Region / segment / line of business / fiscal period
- **Trigger:** Qualified pipeline available for a defined revenue period falls below the coverage level required to achieve target.
- **Business meaning:** Future target attainment may be at risk before the miss appears in recognized revenue.
- **Recommended action:** Diagnose gap by source, segment, stage, seller, and expected realization period; define recovery plan.
- **Owner:** Sales leadership + RevOps
- **Validation required:** Required coverage ratio by business line and horizon.

### S-PIP-002 — Stage Aging / Stalled Opportunity
- **Evidence state:** KNOWN + REPORTED
- **Evidence basis:** Job description requires stage definitions, pipeline progression, deal velocity, and opportunity criteria.
- **Candidate source/system:** CRM opportunity history
- **Entity level:** Opportunity
- **Trigger:** Opportunity remains in a stage materially longer than the validated normal range or lacks required progression evidence.
- **Business meaning:** Close probability, timing, or data quality may be overstated.
- **Recommended action:** Inspect next step, stakeholder engagement, decision criteria, close date, and stage validity.
- **Owner:** Opportunity owner + sales manager
- **Validation required:** Stage-specific aging benchmarks and exit criteria.

### S-PIP-003 — Large-Deal Conversion Risk
- **Evidence state:** REPORTED
- **Evidence basis:** Demetreus reported more $1M+ pursuits while win rate was declining and described a need to improve pursuit effectiveness.
- **Candidate source/system:** CRM + pursuit activity + competitive/deal review data
- **Entity level:** Opportunity
- **Trigger:** Strategic/high-value opportunity shows weak progression, low engagement, competitive disadvantage, or conversion characteristics associated with prior losses.
- **Business meaning:** Concentrated pipeline value may exaggerate attainable revenue.
- **Recommended action:** Initiate executive deal review, validate buying committee, value case, competition, and pursuit strategy.
- **Owner:** Sales leadership
- **Validation required:** Strategic-deal threshold and loss-pattern features.

### S-PIP-004 — Close-Date Credibility Risk
- **Evidence state:** REPORTED
- **Evidence basis:** Forecasting accuracy and opportunity timing were repeatedly identified as core RevOps needs.
- **Candidate source/system:** CRM opportunity history
- **Entity level:** Opportunity
- **Trigger:** Close date is repeatedly moved, unsupported by recent buyer evidence, or inconsistent with normal sales-cycle behavior.
- **Business meaning:** Forecast period placement may be unreliable.
- **Recommended action:** Revalidate close date using buyer-confirmed milestone evidence and historical timing patterns.
- **Owner:** Sales manager + RevOps
- **Validation required:** Push-count and buyer-evidence thresholds.

---

## Domain 2 — Marketing / Demand

### S-MKT-001 — Lead Quality / Sales Acceptance Gap
- **Evidence state:** KNOWN + REPORTED
- **Evidence basis:** Job description requires Marketing/Sales alignment on lead quality and handoffs; Demetreus reported difficulty converting marketing activity into usable feedback.
- **Candidate source/system:** Marketing automation + CRM
- **Entity level:** Lead / campaign / segment
- **Trigger:** Marketing-qualified leads show materially lower sales acceptance or conversion than agreed benchmark.
- **Business meaning:** Spend may be generating volume without sufficient commercial quality.
- **Recommended action:** Review ICP fit, source, qualification logic, rejection reasons, and SLA adherence.
- **Owner:** Marketing + Sales + RevOps
- **Validation required:** MQL/SQL definitions and acceptance benchmarks.

### S-MKT-002 — Campaign Attribution Feedback Gap
- **Evidence state:** REPORTED
- **Evidence basis:** Sarah and Demetreus described difficulty feeding downstream results back to Marketing to determine what is working.
- **Candidate source/system:** Marketing automation + CRM + revenue data
- **Entity level:** Campaign / channel
- **Trigger:** Campaign-generated leads or opportunities cannot be reliably connected to downstream pipeline, revenue, or loss outcome.
- **Business meaning:** Marketing investment decisions lack closed-loop evidence.
- **Recommended action:** Resolve attribution path, source-code integrity, campaign association, and downstream outcome capture.
- **Owner:** Marketing Ops + RevOps
- **Validation required:** Attribution model and acceptable completeness standard.

### S-MKT-003 — ICP Fit Exception
- **Evidence state:** REPORTED
- **Evidence basis:** Demetreus reported CCL has an ICP definition but is not consistently strict in using it to drive acceptance and focus.
- **Candidate source/system:** CRM + enrichment / firmographic source
- **Entity level:** Lead / account / opportunity
- **Trigger:** New prospect materially falls outside validated ICP criteria but enters active pursuit.
- **Business meaning:** Commercial capacity may be diverted toward lower-probability or lower-value demand.
- **Recommended action:** Confirm strategic exception or disqualify / route to alternate motion.
- **Owner:** Sales + Marketing
- **Validation required:** Final ICP fields, thresholds, and exception policy.

### S-MKT-004 — New-Logo Generation Weakness
- **Evidence state:** REPORTED
- **Evidence basis:** Demetreus described new-business acquisition as a major challenge and cited weak outbound and marketing-generated lead performance.
- **Candidate source/system:** CRM + marketing + sales activity
- **Entity level:** Segment / region / period
- **Trigger:** New-logo qualified pipeline creation, outbound conversion, or marketing-sourced new-business creation falls below plan or historical benchmark.
- **Business meaning:** Existing-account performance may mask insufficient future net-new growth.
- **Recommended action:** Diagnose by source, ICP segment, region, rep, campaign, and conversion step.
- **Owner:** Sales + Marketing + RevOps
- **Validation required:** Net-new definition and target benchmarks.

---

## Domain 3 — Account / Expansion

### S-ACC-001 — Existing-Account Expansion Opportunity
- **Evidence state:** REPORTED
- **Evidence basis:** Sarah explicitly reported "trapped value" in existing accounts and the job description requires cross-sell, upsell, and account-expansion insight.
- **Candidate source/system:** CRM + account history + engagement + delivery history
- **Entity level:** Account
- **Trigger:** Existing client exhibits validated characteristics associated with additional product, audience, geography, or program opportunity but lacks active expansion pursuit.
- **Business meaning:** Revenue opportunity may already exist inside the installed client base.
- **Recommended action:** Generate account review with likely expansion path, evidence, missing information, and recommended owner.
- **Owner:** Account Management / Sales
- **Validation required:** Expansion patterns, account hierarchy, product history, and ownership model.

### S-ACC-002 — Account Engagement Deterioration
- **Evidence state:** HYPOTHESIS
- **Evidence basis:** SIE design logic plus stakeholder emphasis on client lifecycle; no validated CCL engagement telemetry yet.
- **Candidate source/system:** CRM activities + program interactions + digital engagement
- **Entity level:** Account
- **Trigger:** Meaningful engagement falls below validated account-specific or segment benchmark.
- **Business meaning:** Expansion, renewal, scheduled delivery, or relationship health could be weakening.
- **Recommended action:** Review account health and determine whether intervention is warranted.
- **Owner:** Account Management
- **Validation required:** Available engagement data and relationship-health definition.

---

## Domain 4 — Finance / Commercial Timing

### S-FIN-001 — Won-but-Unscheduled Revenue Risk
- **Evidence state:** REPORTED
- **Evidence basis:** David and Demetreus described a gap between contract win and delivery/recognition; won contracts may not yet have an executable program date.
- **Candidate source/system:** CRM + contract + project/program system
- **Entity level:** Contract / opportunity / program
- **Trigger:** Contract is won but required delivery/program dates are absent, tentative, or outside the expected realization window.
- **Business meaning:** Contract value may not translate into recognized revenue in the assumed fiscal period.
- **Recommended action:** Confirm delivery plan, client commitment, dependencies, and likely recognition period.
- **Owner:** Operations + Finance + Account owner
- **Validation required:** Contract-to-schedule workflow and standard timing ranges.

### S-FIN-002 — Scheduled Revenue Date Shift
- **Evidence state:** REPORTED
- **Evidence basis:** Sarah described a $900K contract moving between fiscal years because program timing shifted; David described scheduled revenue as a distinct forecast layer.
- **Candidate source/system:** Project/program system + finance forecast
- **Entity level:** Program / contract
- **Trigger:** Scheduled delivery date moves enough to change fiscal-month, quarter, or year recognition.
- **Business meaning:** Forecast and functional performance expectations may change materially even though the client commitment remains intact.
- **Recommended action:** Reforecast revenue, update affected operational/marketing/sales views, document cause, and assess recurrence risk.
- **Owner:** Finance + Operations + RevOps
- **Validation required:** Materiality threshold and authoritative schedule source.

### S-FIN-003 — Pipeline-to-Recognition Window Risk
- **Evidence state:** REPORTED
- **Evidence basis:** Demetreus reported that later in the fiscal year, newly won deals may have too little time to be scheduled and executed before year end.
- **Candidate source/system:** CRM + historical contract-to-delivery cycle + fiscal calendar
- **Entity level:** Opportunity
- **Trigger:** Expected close date plus expected post-sale delivery lead time extends beyond the target recognition period.
- **Business meaning:** Pipeline may be commercially real but unavailable to close the current fiscal-year revenue gap.
- **Recommended action:** Separate booking probability from recognition probability and shift forecast treatment accordingly.
- **Owner:** Finance + RevOps + Sales
- **Validation required:** Lead-time distributions by offering and geography.

### S-FIN-004 — Contract-to-Cash Cycle Delay
- **Evidence state:** REPORTED
- **Evidence basis:** David and Demetreus described the long path from prospect to contract to design/delivery to invoice/cash.
- **Candidate source/system:** CRM + contracts + project system + ERP
- **Entity level:** Account / opportunity / program
- **Trigger:** Any major interval in contract → schedule → delivery → invoice → cash exceeds validated norm or commitment.
- **Business meaning:** Working-capital timing, forecast confidence, and operational intervention may be affected.
- **Recommended action:** Identify the stalled handoff or dependency and assign recovery action.
- **Owner:** RevOps + Operations + Finance
- **Validation required:** Stage timestamps, SLA expectations, and authoritative system boundaries.

---

## Domain 5 — Delivery / Capacity

### S-DEL-001 — Implementation Capacity Constraint
- **Evidence state:** REPORTED
- **Evidence basis:** David reported that faculty/building capacity is generally manageable, while implementation-manager capacity can sometimes become a constraint.
- **Candidate source/system:** Project/resource planning + scheduled program demand
- **Entity level:** Team / region / program / period
- **Trigger:** Scheduled or expected implementation workload exceeds validated available implementation capacity.
- **Business meaning:** Won or scheduled work may be delayed, creating recognition and client-experience risk.
- **Recommended action:** Rebalance resources, prioritize programs, add flexible capacity, or adjust schedule.
- **Owner:** Operations
- **Validation required:** Capacity unit, workload model, and planning horizon.

### S-DEL-002 — Sales-to-Operations Handoff Incomplete
- **Evidence state:** KNOWN
- **Evidence basis:** Job description explicitly requires accurate and timely transfer of statement-of-work, contract, and project data into project-management systems.
- **Candidate source/system:** CRM + contract repository + project system
- **Entity level:** Won opportunity / program
- **Trigger:** Required post-sale handoff data or documents are missing, inconsistent, or late.
- **Business meaning:** Delivery setup and downstream revenue timing may be delayed or error-prone.
- **Recommended action:** Hold handoff exception review, complete missing elements, and identify process root cause.
- **Owner:** Sales + Operations + RevOps
- **Validation required:** Required handoff checklist and SLA.

---

## Domain 6 — Data / Process

### S-DAT-001 — CRM Adoption / Regional Process Exception
- **Evidence state:** REPORTED
- **Evidence basis:** Sarah reported some regions were managing pipeline in spreadsheets rather than CRM; David reported CRM discipline is stronger in the Americas than internationally.
- **Candidate source/system:** CRM audit / activity / pipeline records
- **Entity level:** Region / team / seller
- **Trigger:** Required CRM activity, opportunity, stage, or forecast data falls below completeness or timeliness standard.
- **Business meaning:** Forecasting, attribution, pipeline governance, and global comparability become unreliable.
- **Recommended action:** Identify process gap, reinforce standard, resolve system friction, and monitor remediation.
- **Owner:** Sales leadership + RevOps
- **Validation required:** Required-field, usage, timeliness, and exception standards.

### S-DAT-002 — Definition / Metric Inconsistency
- **Evidence state:** KNOWN + REPORTED
- **Evidence basis:** Job description calls for clear definitions and data standards; stakeholder interviews repeatedly emphasized common definitions.
- **Candidate source/system:** Metric layer / CRM / reporting catalog
- **Entity level:** Metric / stage / process
- **Trigger:** Multiple functions or reports calculate or label the same commercial concept differently.
- **Business meaning:** Leadership can debate the number instead of acting on the business issue.
- **Recommended action:** Reconcile business definition, document governed logic, identify authoritative source, and retire conflicting versions.
- **Owner:** RevOps + Finance / Data as appropriate
- **Validation required:** Governance authority and metric catalog.

### S-DAT-003 — Required Forecast Evidence Missing
- **Evidence state:** HYPOTHESIS
- **Evidence basis:** Forecast discipline is clearly required, but final required evidence by stage/forecast category is not yet known.
- **Candidate source/system:** CRM
- **Entity level:** Opportunity
- **Trigger:** Opportunity is included in a forecast category without the validated evidence required to support that classification.
- **Business meaning:** Forecast confidence may exceed actual deal evidence.
- **Recommended action:** Request missing evidence or downgrade forecast classification.
- **Owner:** Sales manager + RevOps
- **Validation required:** Forecast categories, evidence requirements, and governance rules.

---

## Domain 7 — External / Strategic

### S-EXT-001 — Macroeconomic Demand Risk
- **Evidence state:** REPORTED
- **Evidence basis:** David reported CCL is developing macroeconomic indicator signaling because recent business unpredictability has been high.
- **Candidate source/system:** External economic indicators + internal pipeline / bookings / revenue
- **Entity level:** Region / sector / portfolio
- **Trigger:** Validated external indicators materially deteriorate for sectors or geographies associated with CCL demand and historically precede commercial weakness.
- **Business meaning:** Pipeline generation, client timing, or program execution may weaken before internal lagging indicators reveal it.
- **Recommended action:** Reassess forecast assumptions, sector exposure, messaging, pipeline generation, and account risk.
- **Owner:** Finance + Strategy + RevOps
- **Validation required:** Indicator set, lag relationships, and materiality thresholds.

### S-EXT-002 — Geopolitical / Travel Disruption Risk
- **Evidence state:** REPORTED
- **Evidence basis:** David reported geopolitical events can directly and indirectly affect CCL, including operations and travel.
- **Candidate source/system:** External risk feeds + program schedule + account geography
- **Entity level:** Region / account / program
- **Trigger:** Event or restriction affects geography, travel feasibility, client availability, or delivery conditions for active/scheduled work.
- **Business meaning:** Scheduled delivery and recognized revenue may move even when commercial demand remains intact.
- **Recommended action:** Identify exposed programs/accounts, confirm contingency options, and update forecast timing.
- **Owner:** Operations + Finance + Account team
- **Validation required:** Exposure data and response playbook.

---

# Taxonomy Summary

| Domain | Signal count | Candidate-stage evidence posture |
|---|---:|---|
| Sales / Pipeline | 4 | Mostly KNOWN/REPORTED |
| Marketing / Demand | 4 | Mostly KNOWN/REPORTED |
| Account / Expansion | 2 | REPORTED + HYPOTHESIS |
| Finance / Commercial Timing | 4 | Strongly REPORTED |
| Delivery / Capacity | 2 | KNOWN/REPORTED |
| Data / Process | 3 | KNOWN/REPORTED + HYPOTHESIS |
| External / Strategic | 2 | REPORTED |
| **Total** | **21** | Candidate-stage, not production-ready |

# Design decisions in v0.1

1. **Delivery/Capacity remains a standalone domain.**
   Rationale: CCL's revenue recognition can depend on post-sale execution timing, and Operations can independently create or resolve timing risk.

2. **Finance/Commercial Timing is separate from Sales/Pipeline.**
   Rationale: booking probability and revenue-recognition timing are distinct problems at CCL.

3. **External/Strategic signals are included but kept narrow.**
   Rationale: the CFO explicitly described macroeconomic and geopolitical signaling as relevant to business unpredictability.

4. **No signal receives a production threshold yet.**
   Rationale: thresholds require historical data, system knowledge, business-line segmentation, and stakeholder validation.

5. **No implementation technology is selected.**
   Rationale: business definitions and test scenarios precede CRM, BI, warehouse, automation, or AI decisions.

# Validation priorities

Before operationalization, confirm:
- CCL business-line and product taxonomy.
- CRM opportunity stages and forecast categories.
- authoritative systems for CRM, contracts, schedules/projects, ERP/finance, marketing automation, and resource planning.
- account and organization hierarchy.
- lead/MQL/SQL and ICP definitions.
- contract-to-schedule and schedule-to-recognition cycle times.
- forecast ownership and review cadence.
- post-sale handoff requirements and SLA.
- regional process variations.
- account management / customer success ownership.
- materiality and response-time standards.

# Next step
Test this taxonomy against five concrete CCL commercial scenarios and determine:
- which signals fire;
- whether signals overlap or conflict;
- whether the signal produces a useful action;
- what evidence is missing;
- which signal definitions should be merged, split, removed, or promoted.
