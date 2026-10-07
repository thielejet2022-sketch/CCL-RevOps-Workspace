# Canonical CCL Entities

**Purpose:** Prevent identity drift caused by transcripts, filenames, speech-to-text, autocomplete, or common-name normalization.

## People

| Canonical name | Entity type | Known conflicting variants | Rule |
|---|---|---|---|
| **Demetreus Lancsweert** | CCL stakeholder | Demetrius; transcript/file labels using Demetrius | Always write **Demetreus** in newly authored material. Preserve conflicting spelling only inside verbatim source artifacts or direct quotations. |

## Governance rule
Canonical entity names override non-authoritative transcription metadata for newly authored analysis and governed artifacts.

A source artifact is not silently rewritten. If its metadata contains a conflicting spelling, preserve the source and normalize the entity only in downstream analysis.

Changes to canonical identity require explicit evidence and a governed update to this file.
