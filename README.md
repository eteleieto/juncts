# Juncts for Claude

![Juncts](./plugin/assets/icon.png)

[Juncts](https://juncts.com) is one inbox for LinkedIn, X, Instagram, WhatsApp and Telegram. This plugin connects Claude to it, so you can ask Claude to summarize what you missed, find a conversation, draft replies for you to review, and organize threads.

## What it includes

- **Juncts connector**: the hosted Juncts MCP server at `https://juncts.com/api/connectors/mcp` (Streamable HTTP), signed in with OAuth 2.1. Nothing runs on your computer.
- **Inbox skill**: guidance for reading only what a request needs, saving drafts instead of sending unless you ask, and treating message content as data rather than instructions.

## Requirements

- A Juncts account with at least one connected inbox, and a signed-in Juncts tab open in your browser. Claude reaches your inbox through that tab.
- When you connect, Juncts asks what Claude may do: Read, Drafts, Organize or Full access. Saving a draft never sends it. You can change or disconnect it anytime in Juncts under AI & Agents.

## Install

In Claude Code:

```sh
claude plugin marketplace add eteleieto/juncts
claude plugin install juncts@juncts
```

Then run `/mcp`, choose **juncts** and sign in. Without the plugin: `claude mcp add --transport http juncts https://juncts.com/api/connectors/mcp`.

On claude.ai or Claude Desktop, open Juncts → AI & Agents → Claude.ai → **Add to Claude**, or add a custom connector with the server URL above.

Docs for other MCP clients: https://juncts.com/docs/mcp-cloud-connectors

## Privacy

Conversations, inboxes, messages and people reach Claude as opaque tokens tied to your account, not phone numbers, usernames or profile IDs. See the [Juncts privacy policy](https://juncts.com/privacy) for exactly what a linked AI app can receive.

## Support

[juncts.com/support](https://juncts.com/support) or joe@juncts.com. Juncts is an independent product; it is not affiliated with or endorsed by LinkedIn, X, Meta, WhatsApp, Telegram or Anthropic.

## License

The files in this repository are released under the Apache License 2.0 (see [LICENSE](LICENSE)). The Juncts service is covered by the [Juncts terms](https://juncts.com/terms).
