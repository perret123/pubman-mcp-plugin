# Pubman MCP plugin for Codex

This public Codex plugin connects Codex to the Pubman MCP server. It supplies no credentials and contains no Pubmanager source code or business data.

The first connection opens the Pubman sign-in flow. Use the Firebase account that you use for Pubman; the server enforces the Pubman roles for every action.

## Install

```sh
git clone https://github.com/perret123/pubman-mcp-plugin.git
codex plugin marketplace add /absolute/path/to/pubman-mcp-plugin
codex plugin add pubman-mcp@perret123-pubman
```

Start a new Codex task after installation so it discovers the plugin and its MCP server.

## MCP endpoint

`https://pubman-mcp-dajaryk6hq-oa.a.run.app/mcp`

The endpoint uses Streamable HTTP and OAuth. Its Pubman integration supports permitted owner workflows such as operational reporting, menu proposals, and approved changes.

## Development

The installable plugin is in `plugins/pubman-mcp/`; the marketplace manifest is in `.agents/plugins/marketplace.json`. Validate it before publishing a change:

```sh
python3 /path/to/plugin-creator/scripts/validate_plugin.py plugins/pubman-mcp
```

## License

MIT. See [LICENSE](LICENSE).
