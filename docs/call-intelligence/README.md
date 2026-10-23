# Call Intelligence Framework v0.1 — PROPOSED
Status: draft for JET review, 2026-10-23. Not an approved CCL policy or deployed workflow.

## Purpose
Turn stakeholder conversations into traceable evidence, cross-functional commercial intelligence, explicit decisions and closed-loop action. Avoid standalone summaries that cannot be compared across meetings.

## Operating contract
1. Capture a source with meeting ID, date, participants, purpose, recording/transcript availability, and storage locator.
2. Extract atomic evidence records with timestamp or line citation. Label stakeholder assertions REPORTED; never treat them as independently verified operational facts.
3. Separate interpretation into intelligence records with evidence links, alternative explanations, confidence, business implications and verification status.
4. Derive discovery questions and actions, each linked to evidence/intelligence; assign owner, due date if agreed, and status.
5. Compare across calls. Corroboration is not proof of data validity. Record conflicts without silently reconciling.
6. Review action outcomes and update intelligence states. Preserve superseded versions and source provenance.

## Tools and placement
- GitHub: public-safe framework, schemas, templates, decisions and changelog ONLY.
- Approved private CCL SharePoint/OneDrive: source transcripts, Excel operational workbook and sensitive meeting briefs, after authorization.
- ChatGPT Project: analysis, synthesis, drafting, exploratory questions.
- Notion/OneNote: human-readable working briefs where authorized; not parallel authoritative registers.
- D365/other operational systems: transactional truth once validated and access granted.

**Security boundary:** This GitHub repository is PUBLIC. Do not commit internal CCL documents, names linked to candid observations, transcripts, pipeline/revenue data, contact details, credentials or workbook extracts. Confirm approved retention, recording consent and AI tool policy before operationalizing.

## Entities
Meeting, Evidence, Intelligence, EvidenceLink, Action, Stakeholder, DiscoveryQuestion. See DATA-DICTIONARY.md.

## Quality gates
- Source: reference and capture date present.
- Evidence: one claim per row; quote/paraphrase traceable; reported vs verified explicit.
- Intelligence: at least one evidence link; interpretation distinguished; counterevidence considered.
- Action: owner, next step, lifecycle status; no implicit commitment.
- Publication: confidentiality and access review completed.
- Closure: result recorded; insight confirmed/refined/rejected; follow-up queue updated.

## Pilot
Two interview-based pilot cases have been analyzed in the private working context. Their details are deliberately excluded from this public repository. Excel workbook v3 is a pilot artifact, not a certified system of record. Validate actual workbook headers, IDs, relationships and formula behavior before declaring schema conformance.

## Versioning
v0.1: proposed minimum viable method. Promote only after JET review and a third-call test.
