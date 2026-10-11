# CCL Named Account Tiering Model v0.1
**Status:** PROPOSED / CANDIDATE-STAGE / NOT APPROVED FOR PRODUCTION
**Date:** 2026-10-10
**Workstream:** Account intelligence / SIE interface

## BLUF
Account tier reflects relatively stable **long-term strategic attractiveness**, not transient buying readiness. Every qualified account remains monitored. Readiness and winnability are separate, time-varying assessments. Tier controls coverage investment, not eligibility for intelligence monitoring.

## Evidence and constraints
- REPORTED: Sarah Nabors described trapped value, account segmentation work, and subjective identification of opportunity in September 2026.
- KNOWN (repository governance): candidate-stage SIE architecture is evidence-gated; no CCL-specific production weights, thresholds, ownership, account cardinalities, or automation without authorized internal evidence.
- UNKNOWN: Cortado's actual CCL segmentation, existing ICP and scoring, customer-level profitability, corporate hierarchy, sales capacity, and buying-center boundaries.
- PROPOSED: model below; any example scores or tiers are SYNTHETIC.

## Qualification gate
Before tiering, establish (a) entity identity and parent/subsidiary relationships, (b) plausible CCL solution applicability, (c) viable market/service geography, (d) reasonable commercial eligibility, and (e) no explicit exclusion. Insufficient evidence yields **Research Needed**, not automatic exclusion or low tier.

## Five dimensions (unweighted initially)
Each dimension receives an evidence-supported ordinal assessment 1–5, plus confidence High/Medium/Low/Unknown and source/as-of date.

| Dimension | 1 anchor | 3 anchor | 5 anchor | Evidence |
|---|---|---|---|---|
| Obtainable multiyear revenue opportunity | Narrow, limited opportunity | Several plausible engagements | Large, credible recurring/multi-unit opportunity | Comparable customer economics, leadership populations |
| CCL solution fit | Weak relevance | Several applicable use cases | Strong fit across proven CCL solutions | CCL portfolio, verified challenges |
| Organizational complexity / whitespace | Few reachable buying centers | Multiple units/levels | Many addressable units, regions, levels | Parent hierarchy, workforce, management layers |
| Economic capacity | Constrained / uncertain | Plausible budget | Durable ability to fund programs | Financial statements, workforce and investment indicators |
| Strategic partnership value | Limited broader value | Some reference/learning potential | Exceptional partnership / reference potential | Industry position, access, long-term collaboration |

**Do not sum these ratings into a production score yet.** Preserve raw assessments and uncertainty. Historical CCL data should establish weighting, predictive value, thresholds, and capacity constraints.

## Provisional tier definitions (qualitative, not numerical)
- **Tier 1 / Strategic:** strongest evidenced long-term attractiveness; merits proactive account planning and deeper human coverage.
- **Tier 2 / Priority:** credible material opportunity; targeted coverage plus continuous monitoring.
- **Tier 3 / Qualified universe:** viable but smaller or less certain opportunity; continuous baseline monitoring and signal-triggered investigation.
- **Research Needed:** fit cannot be reliably evaluated; gather evidence before tier assignment.
- **Excluded:** explicit, recorded qualification failure; periodically review exclusion reason where relevant.

**Tier is not account state.** Track separately:
- Fit/tier: slower-moving structural assessment.
- Readiness: Observe → Investigate → Recommend → Learn (per SIE Decision Contract; not current CCL stages).
- Winnability: stakeholder access, incumbent position, competitive differentiation and route to engagement.
- Account lifecycle: prospect, customer, former customer etc. (actual CCL nomenclature UNKNOWN).
- Evidence confidence and freshness.

## Parent and buying-center discipline
Maintain parent-level strategic assessment and child buying-center observations without asserting actual CCL account/entity cardinalities. Parent may be Tier 1 while an individual buying center has no current initiative. Hierarchy, ownership and relationship rules require CCL discovery.

## Continuous monitoring and activation
All qualified tiers receive baseline monitoring. Investment in sources, enrichment, and human review increases with tier. Monitor executive changes, M&A, financial performance (positive and negative), restructuring, talent signals, competitor/incumbent developments, intent and procurement. Preserve event history and counter-signals. Do not equate a signal with buying intent or create opportunities automatically.

## Validation protocol
1. Retrieve Cortado segmentation/ICP artifacts and compare definitions, avoiding duplicate segmentation.
2. Assemble representative won/lost/no-decision and existing-account expansion cohorts.
3. Check actual revenue, gross margin, repeat purchases, cost to serve, account penetration, and regional differences.
4. Blind-rate historical accounts using information available *before* outcomes to avoid hindsight leakage.
5. Test whether each dimension predicts obtainable value and whether tiers distinguish outcomes; assess bias and data completeness.
6. Set tiers and coverage budgets jointly with Sales, Marketing, Finance and Delivery only after evidence.
7. Review tiers on a regular cadence and upon structural change; record overrides and reasons.

## Minimum prototype fields (conceptual, not D365 configuration)
Account ID, canonical name, parent ID, lifecycle category, qualification status/reason, dimension assessments, confidence per dimension, evidence links, as-of date, provisional tier, override reason, last review date, next review date. Signal events, readiness, and winnability should be related but independently versioned.

## Success measures
Coverage of qualified universe; evidence completeness/freshness; proportion with justified tiers; tier stability vs legitimate changes; realized revenue and gross margin by tier; penetration and expansion; time invested per qualified opportunity; signal-to-conversation and signal-to-qualified-opportunity conversion by tier. Avoid treating a tier score as probability of purchase.

## Key decision boundary
This artifact is a **candidate-stage research model**, not an approved change to the existing SIE signal taxonomy, D365, account ownership, or Cortado work. Production scoring is BLOCKED pending CCL evidence.

## Next
Create a synthetic account assessment sheet and compare it against the Fortune 500 seed universe; then reconcile with actual Cortado segmentation once available.

**Resume:** GO ACCOUNT TIERING PILOT
