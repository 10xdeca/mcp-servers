# MCP Servers

Model Context Protocol (MCP) servers for use with Claude Code and other MCP-compatible clients.

## Servers

### `@10xdeca/mcp-kan`

MCP server for [Kan](https://kan.bn) board task management. Provides tools for managing workspaces, boards, lists, cards, labels, checklists, and comments.

**Environment variables:**
- `KAN_API_KEY` (required) — your Kan API key
- `KAN_BASE_URL` (optional) — defaults to `https://kan.bn/api/v1`

### `@10xdeca/mcp-outline`

MCP server for [Outline](https://getoutline.com) wiki. Provides tools for managing documents, collections, comments, users, and revisions.

**Environment variables:**
- `OUTLINE_API_KEY` (required) — your Outline API key
- `OUTLINE_BASE_URL` (optional) — defaults to `https://kb.xdeca.com/api`

## Setup

```bash
npm install
```

## Usage with Claude Code

Add to your `~/.claude/claude_desktop_config.json` or MCP settings:

```json
{
  "mcpServers": {
    "kan": {
      "command": "node",
      "args": ["./packages/kan/index.js"],
      "env": {
        "KAN_API_KEY": "your-api-key"
      }
    },
    "outline": {
      "command": "node",
      "args": ["./packages/outline/index.js"],
      "env": {
        "OUTLINE_API_KEY": "your-api-key"
      }
    }
  }
}
```
