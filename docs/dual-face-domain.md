# Dual Face Domain Pattern

## Recommended Directory Layout

```
/
├── index.html (or framework entry)     # Human Face
├── robots.txt
├── sitemap.xml
├── llms.txt
├── llms-full.txt                       # optional
├── .well-known/
│   ├── agent.json
│   ├── agents.json                     # if multi-agent
│   └── mcp/
│       └── server-card.json            # or equivalent
├── mcp/                                # or /api
│   └── ...                             # live MCP / API endpoints
├── feed.xml
└── content/                            # optional Markdown mirrors
    └── ...
```

## Design Principles

1. **Discoverability first** — Agents should be able to locate the Agent Face from the root without guessing.
2. **Curated over exhaustive** — `llms.txt` and capability manifests should highlight what matters most, not dump every page.
3. **Protocol honesty** — Only declare protocols and endpoints that are actually implemented and maintained.
4. **Evidence readiness** — Design the Agent Face so that observations can be turned into signed Inference Receipts with minimal friction.

## Human Face / Agent Face Separation

The Human Face may be a rich SPA or statically generated site. The Agent Face lives primarily in the root and `.well-known` surfaces and should remain lightweight, stable, and versioned independently where practical.
