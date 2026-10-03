# Tinylawn for ChatGPT and Codex

Bring calls and saved summaries from Tinylawn, an AI receptionist and answering service for landscaping, lawn care, pest control, and other outdoor service businesses, into conversations. Use that context to understand customer needs, plan next steps, or work alongside other enabled tools.

This is a release candidate. Public listing and hosted availability must be confirmed before distribution. The package uses the portable Agent Plugins 1.0.0 layout with root `plugin.json` and `mcp.json`; no skill is bundled for this MCP-only MVP.

## Connect

You need a Tinylawn account with access to the organization whose calls you want to read. The MCP endpoint is `https://app.gettinylawn.com/mcp`. Sign in to Tinylawn and authorize the `calls:read` permission for one organization when the host connects.

The source package contains a portable `streamable-http` remote MCP configuration. ChatGPT local testing can instead use a connection registered in developer mode and a generated package mapped to that real connection. Public ChatGPT and Codex distribution uses a **With MCP** submission to OpenAI's plugin directory. An existing development connection ID is not a public submission.

After installation or connection, start a new conversation with Tinylawn enabled.

## Try it

- “Turn my 10 most recent Tinylawn calls into a follow-up plan.”
- “Find the calls that need a response and prepare an email with my connected tools.”
- “Show the next page of Tinylawn calls.”

`list_calls` supplies the call context. ChatGPT or Codex can reason over it and, when you enable other tools, use it in broader workflows such as drafting follow-ups, checking a calendar, or creating tasks. Those actions are handled by the other tools under their own permissions and confirmation rules.

`list_calls` accepts only `limit` and an opaque `cursor`. The default page size is 20; you can request 1–50. Results are newest first and include spam and archived calls. Use the returned cursor unchanged to continue. A missing saved summary is `null`; no new summary is generated.

Results include call time, duration when available, category, saved summary when available, unread and archived flags, and a link to the call in Tinylawn. Reading leaves the call's unread and archived state unchanged. Tinylawn itself does not message, schedule, or edit calls, and version 1.0.0 does not expose date/search filters, transcripts, recordings, or metrics. Other enabled tools may perform separate actions.

## Data and access

Only calls in the organization authorized during connection are available. Saved summaries may contain information callers provided. Connecting shares requested call metadata and summaries with the OpenAI service you use. Review the permission before authorizing. Disconnect the connector in the host and revoke its grant in Tinylawn under Settings → Integrations → MCP to end access; previously returned chat content remains governed by the host's policies.

[Website](https://gettinylawn.com) · [Support](https://gettinylawn.com/support) · [Privacy](https://gettinylawn.com/privacy) · [Terms](https://gettinylawn.com/terms)

Support: support@gettinylawn.com. Tinylawn is operated by Sumo Labs LLC.
