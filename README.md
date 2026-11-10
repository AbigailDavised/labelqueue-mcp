# LabelQueue — Avery Label Dimensions, Margin & Bleed Layout Engine

[![Official Website](https://img.shields.io/badge/Website-labelqueue.com-blue)](https://labelqueue.com)
[![MCP Registry](https://img.shields.io/badge/MCP_Registry-com.labelqueue%2Fmcp-green)](https://www.mcptry.com/servers/com.labelqueue/mcp)
[![Glama Connector](https://img.shields.io/badge/Glama-Connector-purple)](https://glama.ai/mcp/connectors/com.labelqueue/mcp)

Look up exact Avery & standard sheet label dimensions, pitch, margins & print layout specs.

- **Official Workbench**: [https://labelqueue.com](https://labelqueue.com)
- **Remote MCP Endpoint**: `https://labelqueue.com/api/mcp` (`streamable-http`, read-only, no API key required)
- **Public OpenAPI 3.0**: [https://labelqueue.com/openapi.json](https://labelqueue.com/openapi.json)
- **LLM Context**: [https://labelqueue.com/llms.txt](https://labelqueue.com/llms.txt) · [https://labelqueue.com/llms-full.txt](https://labelqueue.com/llms-full.txt)

## Tools Provided (4 Read-Only Tools)

| Tool Name | Summary |
| :--- | :--- |
| `lookup_avery_label_specs` | Look up exact physical sheet and label geometry (width, height, top/left margins, horizontal/vertical pitch in inches and mm, columns, rows) for Avery US Letter & A4 label codes (5160, 5163, 5164, 5167, 22807, L7160). |
| `lookup_thermal_roll_label_specs` | Look up exact dimensions in inches, mm, and dots (at 203 DPI and 300 DPI) for Zebra, Rollo, Dymo 30252/30334, and Brother thermal label rolls. |
| `diagnose_browser_label_print_drift` | Diagnose progressive row creep when printing sheet labels from Chrome, Edge, Adobe Acrobat, or macOS Preview caused by Fit-to-Page scaling (~94%–97%). |
| `check_barcode_symbology_requirements` | Verify character constraints, check-digit math, minimum X-dimension mil width, and mandatory left/right quiet zones for retail and warehouse barcodes. |

## Connect in 10 Seconds

### Claude Code
```bash
claude mcp add --transport http labelqueue https://labelqueue.com/api/mcp
```

### Cursor / Claude Desktop / Windsurf (`mcp.json`)
```json
{
  "mcpServers": {
    "labelqueue": {
      "type": "streamable-http",
      "url": "https://labelqueue.com/api/mcp"
    }
  }
}
```

### Agent Skill (`skills.sh`)
```bash
npx -y skills@latest add AbigailDavised/labelqueue-mcp -y
```

## License

MIT © [LabelQueue](https://labelqueue.com)
