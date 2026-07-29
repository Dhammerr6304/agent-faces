# Agent Face Taxonomy

Detailed classification of the surfaces that form a complete Agent Face.

## 1. Discovery & Access Control

### robots.txt
Controls crawler access. Modern practice includes Content-Signal and Content-Usage directives that explicitly address AI training and inference use.

### sitemap.xml
Canonical list of URLs for discovery. Still foundational for both traditional search and agent systems.

## 2. Curated Knowledge Maps

### /llms.txt
Proposed standard (Jeremy Howard, 2024; llmstxt.org). Markdown file at the domain root that provides a curated, LLM-friendly overview and link map of the most important content.

Recommended structure:
- H1 with site/project name
- Blockquote summary
- Sections of links with one-line descriptions

Optional companion: `/llms-full.txt` containing the expanded corpus.

### Markdown Mirrors
Serving clean `.md` versions of key pages (or using content negotiation) reduces noise for agents that prefer structured text over HTML.

## 3. Capability & Protocol Manifests

### /.well-known/agent.json
Emerging convention (Agent Web Protocol and related drafts) for declaring domain intent, available actions, authentication requirements, and which agent protocols the site speaks (MCP, A2A, etc.).

### MCP Endpoints
Model Context Protocol servers exposed at predictable paths (commonly `/mcp` or under `/.well-known/mcp/`). Server cards allow discovery of tools and resources.

### OpenAPI / GraphQL
Machine-readable API contracts remain one of the highest-value Agent Face components for any domain that offers programmatic access.

### Multi-agent declarations
`/.well-known/agents.json` or agent-card formats for domains that host multiple distinct agents or services.

## 4. Semantic Structure

JSON-LD and Schema.org markup embedded in pages. Agents that do not speak specialized agent protocols can still extract typed entities and relationships.

## 5. Syndication

RSS, Atom, and structured API feeds continue to serve as reliable, low-friction discovery and update surfaces.

## 6. Advanced Layers

- AI Manifests for guided UI workflows
- Content negotiation (`Accept: text/markdown`)
- Embeddings or vector search endpoints
- Inference Receipt schemas (bridge to ICE)

---

This taxonomy is living. New surfaces will be added as standards converge.
