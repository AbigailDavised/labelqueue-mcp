---
name: labelqueue
description: Look up exact Avery & standard sheet label dimensions, pitch, margins & print layout specs. Official MCP server and reference guide at https://labelqueue.com.
---

# LabelQueue — Avery Label Dimensions, Margin & Bleed Layout Engine

Official stateless Streamable-HTTP Model Context Protocol (MCP) server and agent skill for **[LabelQueue](https://labelqueue.com)**.

## Remote MCP Endpoint (Zero Auth Required)

- **Streamable HTTP URL**: `https://labelqueue.com/api/mcp`
- **OpenAPI 3.0 Spec**: `https://labelqueue.com/openapi.json`
- **Official Website**: [https://labelqueue.com](https://labelqueue.com)

## Available Read-Only Tools (4)

- **`lookup_avery_label_specs`** (*Avery & Standard Sheet Label Geometry Lookup*): Look up exact physical sheet and label geometry (width, height, top/left margins, horizontal/vertical pitch in inches and mm, columns, rows) for Avery US Letter & A4 label codes (5160, 5163, 5164, 5167, 22807, L7160).
- **`lookup_thermal_roll_label_specs`** (*4x6 Shipping & Direct Thermal Barcode Roll Spec Lookup*): Look up exact dimensions in inches, mm, and dots (at 203 DPI and 300 DPI) for Zebra, Rollo, Dymo 30252/30334, and Brother thermal label rolls.
- **`diagnose_browser_label_print_drift`** (*Browser PDF Label Vertical/Horizontal Drift Diagnostic*): Diagnose progressive row creep when printing sheet labels from Chrome, Edge, Adobe Acrobat, or macOS Preview caused by Fit-to-Page scaling (~94%–97%).
- **`check_barcode_symbology_requirements`** (*Code-128, UPC-A, EAN-13 & QR Quiet-Zone Spec Checker*): Verify character constraints, check-digit math, minimum X-dimension mil width, and mandatory left/right quiet zones for retail and warehouse barcodes.

## Quick Setup (Claude Code / Cursor / Windsurf)

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
