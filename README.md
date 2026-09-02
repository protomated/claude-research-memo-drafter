# Research Memo Drafter — Claude Desktop Plugin

A Claude Desktop plugin for solo and small-firm attorneys. One skill (`/research-memo`): Draft a legal research memo that cites only the source documents (cases, statutes, briefs, contracts) you've attached to a workspace folder — no open web search, no case-law database, no citation drawn from general training knowledge. Every citation is anchored to a specific source file and page/paragraph, and any part of the question the sources don't support is flagged, never quietly filled in. Use when you have the authorities on hand and need a first-draft memo built strictly from them.

Distributed free by [Protomated](https://protomated.com).

---

## Repo layout

```text
plugin/           Installable plugin (packaged into .zip)
  .claude-plugin/plugin.json   Identity manifest
  .mcp.json                    Declares filesystem connector requirement(s)
  manifest.json                Display metadata
  prompts/system-prompt.md     Master system prompt — compliance guardrails live here
  skills/research-memo/
    SKILL.md                   The single skill

scripts/
  validate-plugin.mjs          Validates plugin/ structure before packing

.github/workflows/
  validate.yml     Runs on every push/PR — validates plugin structure
  release.yml      Runs on vX.Y.Z tags — builds, checksums, and publishes a GitHub Release
```

---

## Skill

| Skill | What it does |
|---|---|
| `/research-memo` | Draft a legal research memo that cites only the source documents (cases, statutes, briefs, contracts) you've attached to a workspace folder — no open web search, no case-law database, no citation drawn from general training knowledge. Every citation is anchored to a specific source file and page/paragraph, and any part of the question the sources don't support is flagged, never quietly filled in. Use when you have the authorities on hand and need a first-draft memo built strictly from them. |

---

## Development

```bash
npm run validate   # validate plugin/ structure
npm run build      # validate → pack → checksum
npm run release    # build + gh release create (requires gh CLI + repo write access)
```

---

## Part of the Protomated Plugin Marketplace

This plugin also ships via the [Protomated plugin marketplace](https://github.com/protomated/protomated-plugins-official) (git-native install, no zip needed) — install this repo's zip release if you want a pinned version instead.

## License

Apache 2.0. See [LICENSE](LICENSE).
