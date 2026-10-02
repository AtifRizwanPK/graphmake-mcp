# GraphMake MCP server

Let your AI agent make infographics and charts. The agent fills one of 90+
designed [templates](https://graphmake.com/templates) with your data, or writes
a short [GraphMake Script](https://graphmake.com/script); GraphMake renders it
and returns a PNG or SVG, plus a link to edit it in the free GraphMake editor.

Free, no API key, no account. Server URL:

```
https://graphmake.com/api/mcp
```

Remote MCP over Streamable HTTP, so there is nothing to install or run.

## Connect

**Claude Code** (plugin)

```
/plugin marketplace add AtifRizwanPK/graphmake-mcp
/plugin install graphmake@graphmake
```

or directly:

```
claude mcp add --transport http graphmake https://graphmake.com/api/mcp
```

**Codex**

```
codex mcp add graphmake --url https://graphmake.com/api/mcp
```

**VS Code** (Copilot agent mode)

```
code --add-mcp '{"name":"graphmake","type":"http","url":"https://graphmake.com/api/mcp"}'
```

**Cursor**: add to `~/.cursor/mcp.json`

```json
{ "mcpServers": { "graphmake": { "url": "https://graphmake.com/api/mcp" } } }
```

**Claude app** (claude.ai / Claude Desktop): Settings → Connectors → Add
custom connector → paste the URL.

More clients and a live example: https://graphmake.com/mcp

## Tools

| Tool | What it does |
|------|--------------|
| `list_templates` | Find a template: sales reports, dashboards, comparisons, timelines, resumes and more |
| `get_template` | A template's editable text and numbers, as field keys |
| `render_template` | The template filled with your content → PNG or SVG, with an edit-in-GraphMake link |
| `render_infographic` | GraphMake Script → PNG or SVG, with an edit-in-GraphMake link |
| `graphmake_script_reference` | The full script syntax |
| `open_in_editor` | A link that opens the script on the GraphMake canvas |

It can draw titles, KPI cards, big numbers, text, quotes, lists, ratings; bar,
line, area, pie, donut and radar charts; progress bars, percentage rings,
gauges, waffle charts and word clouds; timelines, process steps, funnels,
pyramids and cycles; and world maps shaded by value.

## Try

> Make an infographic of our Q3 numbers: revenue $1.2M, 842 customers, +18%
> growth, monthly revenue 360, 395 and 445K.

> Use a GraphMake template to turn this month's sales summary into a one-page
> report.

## Limits and privacy

30 renders a minute and 500 a day per IP. Renders are not stored; the server
logs which tool was called and whether it worked, not the content.
