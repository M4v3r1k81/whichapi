# Installing whichapi

whichapi is a hosted remote MCP server. Nothing to download or build, no API key.

- Transport: streamable HTTP
- URL: `https://whichapi.dev/mcp?via=github`
- Tool: `find_services` (argument `need`: what you need, in plain words)

Add it to the MCP settings of your client, for example:

```json
{ "mcpServers": { "whichapi": { "url": "https://whichapi.dev/mcp?via=github" } } }
```

Claude Code: `claude mcp add --transport http whichapi https://whichapi.dev/mcp?via=github`

To check it works, call `find_services` with `{"need": "convert scanned pdf to text"}`: it returns a JSON list of
matching services with name, URL, price per call and distinct buyers in the last 30 days.
