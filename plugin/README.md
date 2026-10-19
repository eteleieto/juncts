# Juncts

![Juncts](./assets/icon.png)

Read and summarize connected inboxes, prepare replies for review, and organize conversations from Claude Code or Claude desktop with plugin support. The desktop package starts a bundled Node.js MCP server; the source development plugin starts the exact npm package `juncts-mcp@0.1.1`. Node.js 22 and a signed-in Juncts browser tab are required. In Juncts, enable the appropriate access level in Settings → Agents, keep the app open, and ask Juncts to summarize unread conversations or save reply drafts.

The generated remote variant connects to the explicitly supplied HTTPS MCP endpoint using OAuth discovery instead of starting local code. The remote service must be deployed and tested separately. Private inbox access requires authentication. Available operations are constrained by both OAuth scope and the app’s agent access setting.

## Privacy Policy

[Juncts privacy policy](https://juncts.com/privacy) describes storage, sharing, retention, and deletion. The local server relays operations to the Juncts tab over loopback. The remote variant relays requests through Juncts’ hosted connector service to the signed-in browser session. Conversation content returned by tools is available to the AI client. Never include credentials in the plugin package. Use [Juncts support](https://juncts.com/support) or contact joe@juncts.com for support or privacy questions.

This package has not been submitted to or approved by a directory. Review account, publication materials, and publisher verification are separate requirements.
