# Research Memo Drafter v1.0.0

Initial release.

## What's included

### `/research-memo` — Research Memo Drafter

Draft a legal research memo that cites only the source documents (cases, statutes, briefs, contracts) you've attached to a workspace folder — no open web search, no case-law database, no citation drawn from general training knowledge. Every citation is anchored to a specific source file and page/paragraph, and any part of the question the sources don't support is flagged, never quietly filled in. Use when you have the authorities on hand and need a first-draft memo built strictly from them.

## Setup

Install time: approximately 5 minutes. Connect Filesystem once in Claude Desktop → Settings → Connectors. See `plugin/CONNECTORS.md` for step-by-step instructions.

## Compliance

Requires Claude for Work, Claude Team, or Claude Enterprise. Do not use a consumer Claude plan (Claude Pro or Personal) with confidential matter information. Every output carries the `AI-ASSISTED DRAFT — ATTORNEY REVIEW REQUIRED` header and `Not legal advice` footer. The skill never writes a file or sends an email without your explicit in-conversation confirmation.
