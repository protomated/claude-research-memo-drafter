# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

**Research Memo Drafter** — a Claude Desktop plugin for solo and small-firm attorneys. One skill (`/research-memo`): Draft a legal research memo that cites only the source documents (cases, statutes, briefs, contracts) you've attached to a workspace folder — no open web search, no case-law database, no citation drawn from general training knowledge. Every citation is anchored to a specific source file and page/paragraph, and any part of the question the sources don't support is flagged, never quietly filled in. Use when you have the authorities on hand and need a first-draft memo built strictly from them. There is no runtime code, no MCP server beyond declared connector requirements, and no backend. The product is entirely content: a markdown skill file and JSON manifests.

This repo is the source of truth for this skill's content. It also ships via the [Protomated plugin marketplace](https://github.com/protomated/protomated-plugins-official) — re-sync that repo's copy manually when this one changes.

## Repo layout

```
plugin/           The installable plugin (packaged into .zip)
  .claude-plugin/plugin.json   Manifest validated by scripts/validate-plugin.mjs
  .mcp.json                    Declares filesystem connector requirement(s)
  manifest.json                Plugin display metadata
  prompts/system-prompt.md     Master system prompt — compliance guardrails live here
  skills/research-memo/SKILL.md  The single skill; YAML frontmatter + markdown body
scripts/
  validate-plugin.mjs          Validates plugin/ structure before packing
```

## Commands

```bash
npm run validate   # validate plugin/ structure
npm run build       # validate → pack → checksum
npm run release      # build + gh release create
```

## Compliance constraints — non-negotiable

1. **Confirmation gating**: Claude must show the attorney exactly what it will do and get explicit in-conversation confirmation before sending email, creating calendar events, or writing any file.
2. **Required output wrapper**: every skill output must begin with `AI-ASSISTED DRAFT — ATTORNEY REVIEW REQUIRED` and end with the `Not legal advice` footer.
3. **Plan-tier warning**: consumer-tier Claude (claude.ai Personal / Pro) must not be used with client-privileged content.

Do not weaken these constraints.
