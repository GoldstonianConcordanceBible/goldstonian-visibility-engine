# Proposal: Add receipt_links field to Claim schema

## Type
- [x] schema_change

## Summary
Add optional `receipt_links` to claim objects so agent actions can be audited through receipts/logs.

## Scope
Repos affected:
- gcb-spec

Files affected:
- SCHEMAS/claim.schema.json
- examples/example.claim.json

## Rationale (Mirror → Water → Fire)
- Mirror: Claims sometimes result from agent actions and should be traceable.
- Water: Audit linkage is common across compliance and distributed systems.
- Fire: Receipts strengthen accountability and post-hoc review.

## Compatibility / Migration Notes
Non-breaking addition (optional field).

## Safety / Non-Investment Compliance
- [x] No ROI/profit language
- [x] Improves accountability

## Attestation(s)
(Insert attestation entry reference here)