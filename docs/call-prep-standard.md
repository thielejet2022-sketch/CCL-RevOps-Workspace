# Call Prep Standard v1.0
Approved by JET for personal call preparation — October 13, 2026.
This governs EVA's preparation for JET; it is not an adopted CCL process.

## Command
**BUILD CALL PREP — [person or meeting] — [date/time]. Purpose: [desired discussion].**
Optional: TEST ONLY; PDF; PERSONAL ONLY; BUSINESS ONLY.
Natural-language equivalents are accepted. Default display timezone: America/New_York (ET, with actual daylight-saving offset).
Example: BUILD CALL PREP — Sarah Nabors — today at 3 PM ET. Purpose: discuss trapped value, Cortado's role and how RevOps can help.
A supplied time is user-reported until matched to a live event. TEST ONLY never establishes a real appointment.

## Default deliverable
Show a concise one-page-equivalent Markdown sheet in ChatGPT, approximately 400–600 words maximum. Aim for a two-minute read. Use the [template](../templates/call-prep-sheet.md). No file export is required unless requested. PDF means a rendered, visually verified one-page printable sheet; keep readable type and shorten content instead of shrinking it. Optional supporting links belong after the main sheet.

## Preparation procedure
1. Read current repository governance and relevant project context. Do not resume unrelated paused work or assume employment, authority or an offer.
2. Identify meeting purpose and intended outcome. If absent, derive a reasonable proposed outcome from accessible meeting/context evidence and label the assumption. Ask only if missing context materially prevents useful prep.
3. For a real scheduled call, read primary Calendar within the stated date/window, page all results, and read full event details as needed. Exclude canceled, declined, all-day, focus/planning and draft onboarding items. Never invent a meeting link, attendees or time. If no matching event exists, use JET-reported logistics with that label. Ambiguous events remain unresolved.
4. Match participants by exact normalized email to Airtable People Email, then by unambiguous full name in event details or JET's request. Never first-name-only matching or similar-person substitution. Use canonical names, including Demetreus Lancsweert.
5. Read current schema, matched People records and all linked Relationship Notes. People summaries are supplementary; linked notes are authoritative captured context. Read Detail, Shared On, Evidence Excerpt, Source, Status, Follow-up Prompt and Review / Event Date. Pocket transcripts are optional corroboration, not a dependency.
6. Read relevant current business records, prior commitments and decisions. Cite the source near each material reminder. Separate KNOWN, REPORTED, HYPOTHESIS, ASSUMPTION, SYNTHETIC and UNKNOWN as needed. Do not invent quotes or treat proposed designs as deployed processes. Verify time-sensitive external facts when needed; stop research once it can support the call.
7. Compose the sheet in the fixed order below. Prioritize items that change JET's questions, choices or next action. Suggested questions and examples are recommendations, not established facts.
8. Check names, time zone, source dates, note status, links, evidence labels and length. If a source is unavailable, provide useful supported portions and explicitly identify the missing source; never claim retrieval or completeness.

## Fixed sheet structure
- **Meeting:** subject, date/time ET, join/calendar link if verified, participants and sourced roles, and confirmed/user-reported/test status.
- **Desired outcome:** one sentence.
- **Personal connection:** 2–4 reminders total by default, dated and linked; 1–2 optional natural openers per person, using fewer for group calls.
- **Business context:** up to 3 key prior statements, commitments, decisions or gaps, with attribution/date/source.
- **Priority questions:** 3 questions in recommended order.
- **Your relevant proof:** 1–2 verified JET examples connected to the purpose. Omit if irrelevant or unavailable.
- **Close the call:** next step, owner and timing to establish; never present a proposed owner/deadline as agreed.
- **Important uncertainty:** material evidence gaps or caveats; omit empty boilerplate.

## Relationship evidence rules
Prefer Current notes as last-reported facts dated to Shared On; Current does not mean freshly reconfirmed. Historical notes require explicit past dates. Skip Superseded. Needs clarification may support a question, never an asserted fact; preserve speaker-attribution caveats even when status says Current.
Do not infer names, ages, birthdays, residence changes, arrivals, trip/tournament outcomes or future plans. Ages are as of the source date. Unknown locality or property use stays unknown. Questions may invite an update without presuming an outcome.

## Privacy, persistence and delivery
- Persistent private relationship details remain in Airtable base appEos8J9kEldWjiy, People tblJpbqWDbmyDBhAj and Relationship Notes tbl55P6DEZZZxrddS.
- Store the standard and blank template in GitHub; do not copy private personal notes or filled sheets there by default.
- Requested private sheet exports follow the available file-saving workflow. Do not distribute to anyone else.
- Never send correspondence to attendees, edit invitations, book meetings, or infer authorization for operational changes.
- The manual command does not alter the existing hourly briefing task. Manual/test previews do not mark a meeting Delivered or suppress its automated reminder.
- Meeting Briefing Log tblmDLyVhLKwTguJR is for the existing automatic workflow: key = calendar ID | event ID | RFC3339 instance start; reuse Prepared entries; skip Delivered; mark Delivered only with actual notification.
- Capturing new relationship facts is a separate authorized action under [relationship-note capture](relationship-note-capture.md).

## Project instruction text
When JET says BUILD CALL PREP, follow docs/call-prep-standard.md and templates/call-prep-sheet.md from the current CCL repository. Produce the concise sheet in ChatGPT using current calendar/business evidence and persistent Airtable Relationship Notes. Show logistics/evidence uncertainty, source dates and optional openers. TEST ONLY establishes no live appointment. Export PDF only when requested. Keep personal details private and never send or edit invitations. This instruction is ready to add to ChatGPT Project settings; repository persistence alone does not modify those settings.

## Acceptance checks
- Real call: verified logistics or clearly user-reported; no invented link.
- Test call: prominently TEST ONLY; no delivery-log or calendar mutation.
- Stale event: never described as upcoming.
- Ambiguous participant: no unrelated person's notes.
- Attribution caveat: retained regardless of Current status.
- Source outage: supported partial prep, access gap stated.
