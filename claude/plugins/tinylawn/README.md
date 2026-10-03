# Tinylawn for Claude

Review recent calls and saved summaries from Tinylawn, an AI receptionist
and answering service for landscaping, lawn care, pest control, and other
outdoor service businesses. Prepare follow-up plans grounded in saved calls.

## Connect

You need a Tinylawn account and membership in the organization you authorize.
Add the plugin in Claude, open its Connectors tab, and connect Tinylawn.
The connector uses https://app.gettinylawn.com/mcp and OAuth calls:read.
Sign in to Tinylawn, select one organization, and choose Allow.
On Team and Enterprise, an organization Owner may need to add the connector first.

Skills and the remote connector work in Claude chat and Cowork.
In Claude Code, load the local plugin with --plugin-dir, or add the
tinylawn/tinylawn-plugins marketplace and install tinylawn@tinylawn.
Use /mcp to complete authentication and /tinylawn:review-calls for the skill.
An Anthropic directory listing and this GitHub marketplace are separate
distribution paths. Use the published directory listing when it is available.

## Try it

- Show my two most recent Tinylawn calls.
- Turn my recent Tinylawn calls into a follow-up plan.
- Show the next page of Tinylawn calls.

## Tool and data

list_calls returns calls newest first, with a default page size of 20 and a
maximum of 50. Continue with the returned cursor unchanged. Results include
time, duration, category, saved summary, unread and archived state, and a
Tinylawn link. A missing summary is null. Reading does not change the call.

The plugin sends no credentials in its files and runs no local server,
hooks, or scripts. Requested metadata and saved summaries from the authorized
organization are shared with Claude. Summaries can contain caller-provided
personal information. The plugin itself stores no call data; Tinylawn and
Claude retain data under their respective policies.

Recordings, full transcripts, date/search filters, metrics, and write actions
are unavailable. Messages, scheduling, and other actions belong to separately
enabled tools and their permissions.

Disconnect in Claude and revoke the grant in Tinylawn Settings > Integrations
> MCP to stop future access. Previously returned chat content follows Claude's
retention policy.

Setup: https://gettinylawn.com/help/claude/
Privacy: https://gettinylawn.com/privacy
Terms: https://gettinylawn.com/terms
Support: support@gettinylawn.com

Published by Tinylawn, operated by Sumo Labs LLC. Plugin files are MIT licensed.
