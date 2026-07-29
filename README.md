# Agent Faces

**A Field Guide to Web Pages That Think**

Every website now maintains two parallel interfaces.

## Core Thesis

The contemporary web is undergoing a structural bifurcation. Every domain increasingly exposes two faces:

1. **Human Face** — The rendered HTML/CSS/UI layer optimized for human perception, narrative flow, visual hierarchy, and interactive storytelling.
2. **Agent Face** — The structured, declarative, machine-interpretable surface designed for autonomous agents, large language models, and automated systems to discover, query, reason over, and act upon the site’s knowledge and capabilities.

The term “face” draws from the Chinese 面 (miàn), which denotes both face and surface/mask. The mask is not deception. It is adaptive presentation. Each audience receives an interface matched to its sensory and processing characteristics.

The project root is becoming the public nervous system of a domain.

> Every website has an Agent Face.

---

## Taxonomy of the Agent Face

A practical classification of the surfaces that collectively constitute an Agent Face:

### 1. Discovery & Access Control
- `robots.txt` (with modern Content-Signal / Content-Usage directives)
- `sitemap.xml` (and sitemap index)
- Explicit permissions for AI crawlers and agents

### 2. Curated Knowledge Maps
- `/llms.txt` (and optional `/llms-full.txt`) — the dominant emerging convention for LLM-oriented site summaries and curated link maps
- Clean Markdown mirrors of key pages (`.md` variants)

### 3. Capability & Protocol Manifests
- `/.well-known/agent.json` (Agent Web Protocol and related drafts)
- `/.well-known/agents.json` or agent-card formats (multi-agent / A2A style declarations)
- MCP endpoints and associated server cards (`/.well-known/mcp/...`)
- OpenAPI (or GraphQL) specifications
- Transitional or legacy manifests still probed by some systems

### 4. Semantic Structure
- JSON-LD / Schema.org markup
- Other structured data embeddings that agents can extract without full rendering

### 5. Syndication & Streaming
- RSS / Atom feeds
- Structured API feeds

### 6. Advanced / Emerging Layers
- AI Manifests for UI workflow guidance
- Content negotiation (e.g., `Accept: text/markdown`)
- Embeddings endpoints or vector indexes where relevant
- Inference-oriented metadata

This is not a flat directory of websites. It is a taxonomy of the machine-readable surfaces a domain can expose.

---

## Dual Face Domain Pattern

A clean structural pattern for any domain:

```
example.com/
├── /                          ← Human Face entry (HTML/SPA)
├── robots.txt
├── sitemap.xml
├── llms.txt
├── llms-full.txt              (optional full corpus)
├── .well-known/
│   ├── agent.json
│   ├── agents.json            (if multi-agent)
│   └── mcp/                   (or server-card.json)
├── mcp/ or /api               ← live protocol endpoints
├── feed.xml / feed.atom
└── [selected pages].md        ← Markdown mirrors
```

The project root itself becomes the primary discovery surface for agents.

---

## Connection to Immutable Chain Evidence (ICE)

The logical pipeline:

```
Human Face
    ↓ (narrative / story consumption)
Agent Face
    ↓ (structured observation surface)
Inference Receipts (IR)
    ↓ (signed, hash-chained records of what the agent actually retrieved, reasoned, and acted upon)
ICE Ledger
    (Immutable Chain Evidence — cryptographically anchored permanent record)
```

Humans consume stories.  
Agents consume evidence.  
ICE records the observation itself.

This supplies a natural evidentiary layer for agent activity that remains outside the mutable control of any single operator.

---

## Project Intent

This repository serves as the living field guide and reference implementation home for **Agent Faces**.

### Planned Structure

- `README.md` — Core thesis and taxonomy (this document)
- `docs/` — Expanded field guide entries for each surface
- `examples/` — Reference Dual Face Domain implementations
- `schemas/` — JSON schemas for agent.json, Inference Receipts, and related manifests
- `checklists/` — Agent-readiness checklists and generators

---

## Status

Early formalization (July 2026). The dual-face framing, taxonomy, and ICE pipeline are defined. Reference implementations and expanded documentation are in progress.

---

## License

MIT
