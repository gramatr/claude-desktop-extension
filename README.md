# grāmatr Claude Desktop Extension

> Real-time intelligent context engineering for Claude Desktop, packaged as an Anthropic [Desktop Extension](https://www.anthropic.com/engineering/desktop-extensions) (`.mcpb`).

## Install in 30 seconds

**[⬇ Download gramatr.mcpb (latest)](https://github.com/gramatr/claude-desktop-extension/releases/latest/download/gramatr.mcpb)**

1. Click the download link above.
2. In Claude Desktop, open **Settings → Extensions**.
3. Drop the `gramatr.mcpb` file onto the form.
4. On first connection, the bundled bridge runs OAuth — sign in with the same identity you use at [gramatr.com](https://gramatr.com). No API key, no manual client setup.

The download URL is **stable across releases** — GitHub auto-redirects to the latest tag's asset of that name, so you never have to track the current version. To pin to a specific version, grab `gramatr-v<version>.mcpb` from the [Releases page](https://github.com/gramatr/claude-desktop-extension/releases) instead.

## What this gets you

Every prompt is pre-classified and loaded with an intelligence contract — behavioral directives, quality criteria, and relevant context from past work — before the model responds.

- **System-prompt collapse** — a structured contract replaces the tens of thousands of tokens of behavioral enforcement you'd otherwise hand-maintain
- **Semantic retrieval** — past decisions, preferences, and project state pulled in automatically
- **Consistent behavior** — the same directives and quality gates on every prompt, every session, every tool; each output gated with a recorded PASS/FAIL

## What this repo is

This repository is the **public, reviewable source** for the extension. It mirrors the contents of the `.mcpb` archive so an Anthropic reviewer or user can audit the manifest and the bundled stdio bridge before installing.

- `manifest.json` — the official Anthropic MCP Bundle manifest (schema v0.3)
- `bin/gramatr-proxy.js` — bundled local stdio bridge that forwards JSON-RPC to `api.gramatr.com/mcp` and performs MCP OAuth itself (RFC 9728 discovery + RFC 8414 metadata + Dynamic Client Registration + PKCE / RFC 8628 device-code)
- `icon.png` — extension icon
- `LICENSE` — grāmatr License v1.0

The mirror is generated automatically from the [gramatr monorepo](https://github.com/gramatr/gramatr) release pipeline; do not open PRs against this repo directly.

## Learn more

- Product: <https://gramatr.com>
- Source (monorepo): <https://github.com/gramatr/gramatr>
- Anthropic Desktop Extensions: <https://www.anthropic.com/engineering/desktop-extensions>

## Version

0.32.25
