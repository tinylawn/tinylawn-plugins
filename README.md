# Tinylawn plugins

Distribution packages for Tinylawn's Claude and OpenAI integrations.
Both use https://app.gettinylawn.com/mcp and organization-scoped OAuth calls:read.

## Claude

The Tinylawn plugin is published in the Anthropic Directory.
[Install Tinylawn in Claude](https://claude.ai/customize/plugins/id/f13e8f75-6d7a-40c5-b34d-12415a09fb78%40anthropic-plugin-directory),
choose **Add**, then open the plugin's **Connectors** tab to add and connect
`tinylawn`. Sign in to Tinylawn and allow access to one organization. The workflow
skill reviews saved call context and helps prepare follow-up plans. See the
[Claude setup guide](https://gettinylawn.com/help/claude/) for plan requirements
and data handling.

For GitHub-based Claude Code installation, the package is in
`claude/plugins/tinylawn`. Add the `tinylawn/tinylawn-plugins` marketplace and
install `tinylawn@tinylawn`.

## ChatGPT and Codex

The portable package is in `openai/plugins/tinylawn`.
[Install Tinylawn in ChatGPT](https://chatgpt.com/plugins/plugin_asdk_app_6aa557b6e54081918e8b7b2f4da0be4c)
from its published listing. This repository does not replace that listing.
The OpenAI marketplace catalog is a package-testing source.

## Maintenance

These files are reviewed exports generated from Tinylawn's private canonical
source. Changes are prepared there and exported here for release.
The MCP server and its access controls are hosted separately.

## License and support

Distribution files are MIT licensed. Tinylawn is operated by Sumo Labs LLC.
Support: support@gettinylawn.com
Privacy: https://gettinylawn.com/privacy
Terms: https://gettinylawn.com/terms
