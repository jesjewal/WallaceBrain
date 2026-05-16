---
name: Adobe for Creativity MCP Connector
description: Status and workarounds for Adobe for creativity connector in Claude Code CLI vs web app
type: reference
---

`claude mcp list` shows `claude.ai Adobe for creativity: https://adobe-creativity.adobe.io/mcp - ✓ Connected` but the tools (adobe_mandatory_init, asset_add_file, image_apply_preset, etc.) do not surface in Claude Code CLI context — ToolSearch returns nothing for them.

**Root cause:** The `claude.ai` connectors are web app integrations (configured via Claude.ai settings). Even when listed as connected in `claude mcp list`, their tools aren't injected into the CLI session tool registry the same way local MCP servers are.

**Workaround:** Run photo editing workflows from Claude.ai web app or Claude Desktop where the connector is confirmed working.

**What was tried:**
- `claude mcp add --transport http` to `creativity-mcp.adobe.io/mcp` → 403 (needs IMS Bearer token)
- `adobe-express-developer` npm MCP → removed (no Adobe Express subscription)
- `/restart` slash command → not responding in current setup
- ToolSearch repeatedly for adobe_mandatory_init → not found

**The adobe-batch-edit-photos skill** at `~/.claude/skills/adobe-batch-edit-photos/` is installed and ready. It will work once run from Claude.ai web app with the connector active.
