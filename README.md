# Helpmonks MCP Server

> Team email and customer support, accessible via AI. Manage your shared inbox with natural language.

Helpmonks is a hosted MCP server that connects any MCP-compatible AI tool to your Helpmonks shared inbox. Read conversations, send replies, assign emails, add labels, manage contacts, and triage your support queue — all via natural language.

## Features

- **Conversation management** — read, reply, assign, and close email threads
- **Team collaboration** — internal notes, assignments, and status updates
- **Contact management** — search and manage customer contacts
- **Label & filter** — organise conversations by labels and status
- **29 tools** — full shared inbox operations via natural language
- **Two data centers** — US (`mcp.helpmonks.com`) and EU (`mcp-eu.helpmonks.com`)

## Quick Start

1. Sign up at [helpmonks.com](https://helpmonks.com) to get your access token
2. Add to your MCP client config:

### Claude Desktop / Cursor / any MCP client

```json
{
  "mcpServers": {
    "helpmonks": {
      "url": "https://mcp.helpmonks.com/sse",
      "headers": {
        "access-token": "YOUR_ACCESS_TOKEN"
      }
    }
  }
}
```

### EU Data Center

```json
{
  "mcpServers": {
    "helpmonks": {
      "url": "https://mcp-eu.helpmonks.com/sse",
      "headers": {
        "access-token": "YOUR_ACCESS_TOKEN"
      }
    }
  }
}
```

## Available Tools (29 total)

### Conversations
- `list_conversations` — list inbox conversations with filters
- `get_conversation` — get full conversation with all emails and notes
- `create_conversation` — create a new conversation
- `reply_to_conversation` — send a reply email
- `update_conversation_status` — open, close, archive, or mark as spam

### Team & Organisation
- `update_conversation_assignee` — assign to a team member
- `update_conversation_labels` — add or replace labels
- `add_conversation_note` — add internal or public notes
- `delete_conversation_note` — remove a note

### Contacts & Mailboxes
- `list_contacts` — search and list contacts
- `get_contact` — get contact details
- `list_mailboxes` — list all mailboxes
- `list_team_members` — list team members

[Full tool reference →](https://helpmonks.com/docs/mcp)

## Authentication

All requests require an `access-token` header. Get your token from your Helpmonks account settings.

## Data Centers

| Region | URL |
|---|---|
| US | `https://mcp.helpmonks.com/sse` |
| EU | `https://mcp-eu.helpmonks.com/sse` |

## License

AGPL-3.0 — see [LICENSE](LICENSE)
