# Agent Exports (index/exports)

This folder contains **agent-readable canonical dumps**.
These exports are the primary ingestion surface for AI agents, search tools, and automated content pipelines.

## Export Files
- `canon.export.json` — pointers + summaries of canonical artifacts
- `claims.export.json` — structured claims list with provenance
- `glossary.export.json` — structured glossary terms
- `media.export.json` — structured media registry
- `governance.export.json` — structured governance registry
- `knowledge-graph.export.json` — node/edge graph of concepts, claims, media, and governance

## Rules
1. Every export must declare `canon_version`.
2. Every exported object should include a `provenance` block where possible.
3. Media and governance objects must link back to canonical refs + release tags + DOI when available.