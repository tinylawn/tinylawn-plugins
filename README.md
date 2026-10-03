# Tinylawn plugins

Distribution packages for Tinylawn's Claude and OpenAI integrations.
Both use https://app.gettinylawn.com/mcp and organization-scoped OAuth calls:read.

## Claude

The plugin is in claude/plugins/tinylawn. Add the tinylawn/tinylawn-plugins
marketplace in Claude Code and install tinylawn@tinylawn. The workflow skill
reviews saved call context and prepares follow-up plans. See the plugin README
and https://gettinylawn.com/help/claude/ for setup and data handling.

## ChatGPT and Codex

The portable package is in openai/plugins/tinylawn. ChatGPT users should use
the existing Tinylawn listing. This repository does not replace that listing.
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
