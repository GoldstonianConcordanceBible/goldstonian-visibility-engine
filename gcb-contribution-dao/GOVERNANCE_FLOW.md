# Governance Flow (Proposal → Review → Attestation → Release)

Contract Address (pump.fun):
E68E27Y72FHTJH1MycB6KjX5PQAyKPYsRGZjMEx9pump

## 1) Create a Proposal
- Copy `PROPOSAL_TEMPLATE.md` into `proposals/NNNN-title.md`
- Use next available number (zero-padded)
- Fill Mirror/Water/Fire rationale

## 2) Open a PR
- PR must link the proposal file
- PR must list affected repos and files

## 3) Review
Use `REVIEW_CHECKLIST.md` to validate:
- canon alignment
- glossary lock
- safety/non-investment framing
- schema validation (if JSON artifacts)
- provenance preservation

## 4) Attestation
Add an entry to `ATTESTATION_LOG.md`:
- author attestation (required for most changes)
- reviewer attestation (required for canon/spec)

## 5) Merge
Maintainer merges PR if:
- proposal is complete
- checklist passes
- attestations are recorded

## 6) Release (if required)
If canon/spec meaning changes:
- bump version in affected repo(s)
- tag release `vMAJOR.MINOR.PATCH`
- update changelog/deprecations
- reference proposal ID in release notes