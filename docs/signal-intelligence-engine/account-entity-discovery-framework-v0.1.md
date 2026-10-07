# CCL Account / Entity Discovery Framework v0.1

**Status:** PROPOSED
**Stage:** Candidate / pre-employment
**Updated:** 2026-10-07
**Purpose:** Define what must be discovered before creating a CCL Account/Entity Model. This is a discovery framework, not a representation of CCL's current data model.

## Design boundary
This artifact does **not** define Dynamics 365 objects, cardinality, system-of-record ownership, account hierarchy, or final CCL terminology.

Its job is to turn SIE requirements into structured discovery questions so future modeling is evidence-led.

## Evidence currently available

### REPORTED / supported concepts
Stakeholder interviews and the RevOps role context support the existence or commercial relevance of:
- clients / organizations;
- people involved in buying and relationship activity;
- sales opportunities / pipeline;
- contracts / commercial commitments;
- delivery/program activity;
- multiple lines of business / offerings;
- geography / regions;
- marketing sources and campaigns;
- sales/account ownership;
- scheduled and recognized revenue.

These concepts do not establish how CCL represents them technically or how they relate cardinally.

## Candidate lifecycle skeleton

The following is a **HYPOTHESIS FRAMEWORK**, not a CCL fact:

Organization / Client
→ People / Stakeholders
→ Commercial Opportunity
→ Contract / Commitment
→ Delivery / Program
→ Revenue Realization

Contextual dimensions may include:
- Offering / line of business
- Geography / region
- Marketing source / campaign
- Commercial / account ownership

The sequence is useful for discovery because SIE must connect commercial evidence across the lifecycle. It must not be interpreted as a final object model.

## Discovery domains

### 1. Organization / Account
**Why SIE needs it:** Account intelligence, expansion, pipeline aggregation, relationship history, prioritization.

**UNKNOWN**
- What is the canonical CCL definition of client/account?
- Is a global organization represented once or as multiple regional/legal/business-unit accounts?
- How are parent/subsidiary/division relationships represented?
- How are duplicate organizations resolved?
- How are former, current, and prospective clients distinguished?
- What entity anchors enterprise-wide relationship history?

**Validation evidence needed:** CRM account records, hierarchy rules, data dictionary, representative global-account walkthroughs.

### 2. People / Stakeholders
**Why SIE needs it:** Buying committee, relationship strength, engagement, influence, account continuity.

**UNKNOWN**
- What person/contact entity exists?
- Can a person relate to multiple organizations?
- Are buying roles, influence, executive sponsorship, or relationship roles captured?
- How are job changes handled?
- Are Marketing and Sales identities reconciled to the same person?

**Validation evidence needed:** Contact schema, relationship roles, campaign/CRM identity logic, sample account walkthrough.

### 3. Opportunity / Pipeline
**Why SIE needs it:** Pipeline signals, forecast, pursuit risk, commercial/booking lens.

**REPORTED:** Pipeline and forecasting are central RevOps concerns.

**UNKNOWN**
- What creates an opportunity?
- What stages/categories exist?
- What is the grain of an opportunity?
- Can one opportunity cover multiple offerings, programs, regions, or contracts?
- How are new-logo and expansion opportunities distinguished?
- What evidence supports stage and forecast classification?

**Validation evidence needed:** Opportunity schema, stage definitions, forecast process, sample won/lost deals.

### 4. Contract / Commercial Commitment
**Why SIE needs it:** Separates commercial win from delivery and revenue realization.

**REPORTED:** Stakeholders described a meaningful gap between contract win and revenue recognition.

**UNKNOWN**
- What event constitutes booking/contract commitment?
- Is contract a distinct system entity?
- Can one opportunity produce multiple contracts?
- Can contracts be amended, extended, or partially fulfilled?
- Where are value, term, obligations, and effective dates authoritative?

**Validation evidence needed:** Contract workflow, system ownership, sample opportunity-to-contract trace.

### 5. Delivery / Program
**Why SIE needs it:** Scheduled revenue, capacity, handoff, realization timing.

**REPORTED:** Delivery timing materially affects revenue realization and differs by business line.

**UNKNOWN**
- Is "program" a universal delivery concept?
- Does coaching, licensing, open enrollment, and custom solutions use the same delivery grain?
- Can one contract create multiple delivery units?
- How are schedule changes recorded?
- What entity links delivery to contract and recognized revenue?
- What resource/capacity entities matter?

**Validation evidence needed:** Delivery/project systems, line-of-business walkthroughs, schedule and resource data.

### 6. Offering / Line of Business
**Why SIE needs it:** Different sales cycles, delivery patterns, capacity requirements, and revenue timing may require different signal logic.

**REPORTED:** CCL operates multiple lines of business with different recognition/delivery patterns.

**UNKNOWN**
- What is the governed offering hierarchy?
- Are products, services, programs, solutions, and lines of business separate concepts?
- At what level should signals and forecasts segment behavior?
- How are bundled/multi-offering deals represented?

**Validation evidence needed:** Product/service catalog, finance hierarchy, CRM offering structure.

### 7. Marketing Source / Campaign
**Why SIE needs it:** Attribution, lead quality, ICP fit, closed-loop Marketing feedback.

**REPORTED:** Source codes and Marketing channels exist, while downstream feedback is incomplete.

**UNKNOWN**
- What is the campaign/source hierarchy?
- How are people/accounts/opportunities attributed?
- What attribution model is used?
- What IDs persist across Marketing and CRM?
- Can outcomes be traced back to source reliably?

**Validation evidence needed:** Marketing automation model, CRM campaign/source fields, attribution reporting.

### 8. Geography / Region
**Why SIE needs it:** Regional process variation, ownership, forecast, delivery, external risk.

**REPORTED:** CRM/process discipline varies regionally.

**UNKNOWN**
- What is the official region/geography hierarchy?
- Is geography attached to client, seller, opportunity, delivery location, or several entities?
- How are global accounts owned across regions?
- Which geography drives reporting and forecasting?

**Validation evidence needed:** Territory/region definitions, ownership rules, reporting hierarchy.

### 9. Ownership
**Why SIE needs it:** Every recommendation requires an accountable human or function.

**UNKNOWN**
- Who owns account, opportunity, relationship, delivery, and post-sale expansion?
- Can ownership be shared across region/offering?
- What happens when commercial and delivery ownership differ?
- What escalation path exists for cross-functional signals?

**Validation evidence needed:** RACI/role definitions, CRM ownership, sales/account-management process.

### 10. Revenue / Financial realization
**Why SIE needs it:** CCL's SIE explicitly distinguishes commercial/booking forecast from revenue realization.

**REPORTED:** Actual, scheduled, contracted, and pipeline revenue represent materially different commercial states.

**UNKNOWN**
- What are the authoritative financial entities and measures?
- What links contract/delivery to recognized revenue?
- What recognition grain exists by line of business?
- How are reschedules, cancellations, credits, and amendments represented?
- What fiscal/calendar dimensions govern forecast placement?

**Validation evidence needed:** Finance definitions, ERP/project relationship, revenue-recognition walkthrough by business line.

## Critical relationship questions
Before an Account/Entity Model is approved, explicitly determine:
1. Organization ↔ Organization: hierarchy and identity resolution.
2. Organization ↔ Person: affiliation and relationship history.
3. Organization ↔ Opportunity: account grain and ownership.
4. Opportunity ↔ Contract: one-to-one, one-to-many, or other.
5. Contract ↔ Delivery: fulfillment structure by line of business.
6. Delivery ↔ Revenue: schedule and recognition linkage.
7. Campaign/Source ↔ Person/Organization/Opportunity: attribution path.
8. Offering ↔ Opportunity/Contract/Delivery: commercial and fulfillment grain.
9. Geography ↔ Organization/Opportunity/Delivery/Owner: reporting and responsibility.
10. Owner ↔ Account/Opportunity/Delivery: action accountability.

All cardinalities are **UNKNOWN** until validated.

## SIE dependency map
The discovery priority should follow signal usefulness rather than data-model elegance.

**Tier A: needed for current Tier-1 SIE validation**
- Opportunity / pipeline
- Contract / commercial commitment
- Delivery / schedule
- Revenue / fiscal period
- Marketing source / campaign
- Geography / region
- Ownership

**Tier B: needed for richer account intelligence**
- Organization hierarchy
- People / buying roles
- Offering hierarchy

**Tier C: needed before expansion scoring**
- Account identity resolution
- Purchase/delivery history
- Buying-center relationships
- Offering whitespace
- Account ownership
- Validated expansion outcomes

## Recommended Day-0 discovery walkthrough
Ask CCL to select representative real examples and trace them across systems:

1. A new-logo pursuit from Marketing source → opportunity → contract → delivery → recognized revenue.
2. An existing-client expansion pursuit through the same lifecycle.
3. A global or structurally complex client to expose hierarchy/ownership rules.
4. A contract whose delivery moved across fiscal periods.
5. One example from each materially different line of business.

For each walkthrough capture:
- CCL terminology;
- entity/object used;
- unique identifier;
- authoritative system;
- owner;
- upstream/downstream relationships;
- timestamps;
- exceptions/manual work;
- reporting consequences;
- missing or unreliable data.

## Exit criteria for creating Account/Entity Model v0.1
Do not promote this discovery framework into an Account/Entity Model until:
- canonical account/client definition is understood;
- core lifecycle entities and identifiers are observed;
- major relationship cardinalities are validated;
- authoritative systems are identified;
- offering/line-of-business differences are understood;
- ownership and regional rules are understood enough to avoid false hierarchy;
- commercial booking and revenue realization can be traced end to end.

## Current conclusion
**KNOWN:** SIE requires connected commercial entities across the client lifecycle.

**REPORTED:** CCL has cross-functional gaps involving pipeline, Marketing feedback, delivery timing, regional CRM/process consistency, and revenue realization.

**HYPOTHESIS:** A connected account/entity layer can provide the backbone for account intelligence and signal reasoning.

**UNKNOWN:** CCL's actual domain structure, cardinalities, terminology, object model, and system-of-record boundaries.

**Recommended test:** Evidence-led lifecycle walkthroughs using real CCL examples before modeling.
