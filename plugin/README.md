# Research Memo Drafter for Law Firms — Claude Desktop Plugin

A Claude Desktop plugin for solo and small-firm attorneys. One skill (`/research-memo`): Draft a legal research memo that cites only the source documents (cases, statutes, briefs, contracts) you've attached to a workspace folder — no open web search, no case-law database, no citation drawn from general training knowledge. Every citation is anchored to a specific source file and page/paragraph, and any part of the question the sources don't support is flagged, never quietly filled in. Use when you have the authorities on hand and need a first-draft memo built strictly from them.

**Distributed by [Protomated](https://protomated.com) as a free download.**

---

## ⚠️ Required: Read This Before You Install

### 1. You must be on a qualifying Claude plan

Do NOT use this plugin for client work on a consumer Claude plan (claude.ai Personal or Claude Pro). Consumer plans do not provide a Data Processing Agreement (DPA) covering client-privileged content. Use **Claude for Work**, **Claude Team/Enterprise**, or the **Claude API** with a signed DPA.

### 2. Every AI output requires your review

Every document this plugin generates must be reviewed and approved by you, a licensed attorney, before use. The plugin enforces this with a required header and footer on every output: `⚠️ AI-ASSISTED DRAFT — ATTORNEY REVIEW REQUIRED`.

### 3. No action without your confirmation

The plugin is instructed to request your explicit in-conversation confirmation before writing any file or sending any email.

---

## Installation (under 5 minutes)

### Step 1 — Download and install

1. Download `research-memo-drafter.zip` from the [Releases page](https://github.com/protomated/claude-research-memo-drafter/releases).
2. Double-click the `.zip` file, or drag it into Claude Desktop's **Extensions** panel.
3. Claude Desktop will install the plugin and prompt you to connect the required connector(s).

### Step 2 — Connect Filesystem

See [CONNECTORS.md](CONNECTORS.md) for step-by-step setup and troubleshooting.

### Step 3 — Verify

Open a new Claude Desktop chat. Type `/skills`. You should see `/research-memo` listed. Run it to start.

---

## The Skill

### `/research-memo` — Research Memo Drafter

Draft a legal research memo that cites only the source documents (cases, statutes, briefs, contracts) you've attached to a workspace folder — no open web search, no case-law database, no citation drawn from general training knowledge. Every citation is anchored to a specific source file and page/paragraph, and any part of the question the sources don't support is flagged, never quietly filled in. Use when you have the authorities on hand and need a first-draft memo built strictly from them.

---

## License

Apache 2.0. See [LICENSE](LICENSE).

## Feedback and Issues

[GitHub Issues](https://github.com/protomated/claude-research-memo-drafter/issues) | [hello@protomated.com](mailto:hello@protomated.com)
