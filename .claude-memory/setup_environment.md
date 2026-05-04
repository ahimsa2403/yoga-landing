---
name: Claude Code environment setup
description: MCPs and skills the user expects available — for reproducing on a new machine
type: reference
---

User's Claude Code environment as of **2026-05-04**.

## MCP servers (3 local + 3 remote)

Local (npx, install with `claude mcp add`):
```
claude mcp add context7 -- npx -y @upstash/context7-mcp@latest
claude mcp add memory-keeper -- npx -y mcp-memory-keeper
claude mcp add chrome-devtools -- npx -y chrome-devtools-mcp
```

Remote (HTTP transport, then `/mcp` to authenticate inside Claude Code):
```
claude mcp add --transport http "claude.ai Google Drive" https://drivemcp.googleapis.com/mcp/v1
claude mcp add --transport http "claude.ai Gmail" https://gmailmcp.googleapis.com/mcp/v1
claude mcp add --transport http "claude.ai Google Calendar" https://calendarmcp.googleapis.com/mcp/v1
```

Chrome DevTools MCP needs Google Chrome installed.

## Skills (20, all from `anthropics/claude-plugins-official` marketplace)

Marketplace setup:
```
claude plugin marketplace add anthropics/claude-plugins-official
```

Installed skill names (in `~/.claude/skills/`):
banner-design, bencium-impact-designer, brand, canvas-design, composition-patterns,
contrast-checker, design, design-audit, design-system, frontend-design, link-purpose,
react-best-practices, refactor, slides, theme-factory, ui-styling, ui-ux-pro-max,
use-of-color, web-artifacts-builder, web-design-guidelines

## Built-in (no install needed)
init, review, security-review, loop, schedule, simplify, fewer-permission-prompts,
update-config, keybindings-help, claude-api

**Why:** User worked across two devices and wanted reproducibility.
**How to apply:** When user moves machines or reports a missing skill/tool, refer here. Replaces stale `setup_uiux_skills.md`.
