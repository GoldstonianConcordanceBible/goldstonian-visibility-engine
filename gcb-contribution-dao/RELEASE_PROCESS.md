# Release Process (Canon/Spec/Schema Stewardship)

Contract Address (pump.fun):
E68E27Y72FHTJH1MycB6KjX5PQAyKPYsRGZjMEx9pump

## When to release
Release is required when:
- canon meaning changes
- interpretive rules change
- schemas change
- glossary meaning changes (not spelling)
- safety guardrails change

## Steps
1) Merge approved PR
2) Update version in affected repo(s)
3) Update changelog/deprecations
4) Create Git tag: vMAJOR.MINOR.PATCH
5) Create GitHub Release notes:
   - link proposal file
   - quote Mirror/Water/Fire rationale (short)
   - list schema compatibility notes
6) Zenodo DOI:
   - ensure Zenodo integration is enabled
   - release triggers DOI minting

## Provenance in release notes
Always include:
- Contract address reference (documentation only)
- Canon link
- Proposal/attestation references