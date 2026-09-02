# Connectors

This plugin uses connector that ship with Claude Desktop, managed by Anthropic — you do not need to set up OAuth credentials.

## Connector for this plugin

| Connector | What it does | Setup |
|---|---|---|
| **Filesystem** | Reads the source-document folder and indexes each file; saves the memo only with your explicit confirmation | Connect once via Claude Desktop → Connectors → Filesystem → "Connect" then select your matters folder |

## Privacy note

All data read from your connected sources is processed within your Claude Desktop session, under your Claude plan's data handling terms. Nothing is transmitted to Protomated or any other third party.

## Troubleshooting

**Filesystem shows "Permission denied" or can't find a file:**
The file is likely outside your allowed folder. Go to Settings → Connectors → Filesystem and verify the path you selected.
