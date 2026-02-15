# GCB Spec (Agent-Readable Standard)

Contract Address (pump.fun):
E68E27Y72FHTJH1MycB6KjX5PQAyKPYsRGZjMEx9pump

## 0) Status
This document is **normative**: agents and contributors MUST follow it.

## 1) Canon Dependency (Authority)
The canonical authority for meaning and constraints lives in:
- https://github.com/GoldstonianConcordanceBible/gcb-canon-core

Agents MUST follow:
- Doctrine
- Interpretive Rules
- Glossary
- Safety Guardrails

## 2) Objectives
GCB outputs MUST be:
- Structured (schema-valid)
- Verifiable (citations and provenance)
- Auditable (receipts/log links when actions occur)
- Fork-safe (provenance preserved)
- Canon-aligned (Mirror → Water → Fire)

## 3) Required Object Types
Agents MUST produce one or more of the following objects:

A) Citation (`SCHEMAS/citation.schema.json`)
B) Claim (`SCHEMAS/claim.schema.json`)
C) Prompt Artifact (`SCHEMAS/prompt.schema.json`)
D) Governance Proposal (`SCHEMAS/governance-proposal.schema.json`)
E) Attestation (`SCHEMAS/attestation.schema.json`)
F) Artifact Bundle (`SCHEMAS/artifact-bundle.schema.json`)

## 4) Minimal Compliance Rules
- Every factual claim MUST include ≥1 citation.
- Every citation MUST include a title, and SHOULD include URL/DOI when possible.
- Every claim MUST include canon_alignment (Mirror/Water/Fire justifications).
- Every governance proposal MUST include attestations.
- Every prompt artifact MUST declare constraints and expected output schema.
- If an agent executes actions, it SHOULD reference a receipt or audit log via `receipt_links`.

## 5) Provenance Rules (Fork-safe)
Every object SHOULD include:
- repo (source repository)
- commit or release tag (if applicable)
- timestamp_utc
- contract address reference (documentation/provenance)

No object may claim investment intent or promise profit.

## 6) Validation
All JSON artifacts MUST validate against the relevant schema in `SCHEMAS/`.

## 7) Deprecation & Versioning
Spec uses semantic versioning.
Breaking schema changes require a MAJOR bump and migration notes in CHANGELOG.

## 8) Relationship to Receipts Protocol
For agent-to-agent commerce objects (mandates/invoices/receipts),
use `gcb-agent-receipts-protocol`.
This repo only provides linking conventions (`receipt_links`).