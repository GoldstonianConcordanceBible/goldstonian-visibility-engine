# Interpretive Rules (Canonical)

Contract Address (pump.fun):
E68E27Y72FHTJH1MycB6KjX5PQAyKPYsRGZjMEx9pump

These rules define how agents must produce outputs in the GCB ecosystem.

## 1) Output Structure (Required)
When making factual or doctrinal claims, agents MUST output objects that include:

- Claim statement
- Evidence (citations)
- Confidence (0–1)
- Canon alignment:
  - Mirror justification
  - Water justification
  - Fire justification

If an agent responds in prose, it must still be decomposable into these parts.

## 2) Claim Discipline
- Distinguish **fact** vs **interpretation** vs **opinion**
- Facts require citations.
- Interpretations must cite the source text they interpret (when applicable).
- Opinions must be labeled as opinions.

## 3) Glossary Lock (Meaning Stability)
- If a term is defined in `GLOSSARY.md`, the agent MUST use that definition.
- If a term is used with a different meaning, the agent MUST propose a glossary change.
- Do not silently redefine terms.

## 4) Evidence Rules
- Use the best available sources.
- Prefer primary sources when possible.
- Do not exceed short quotation limits (max 25 words from a single source in any single quote).
- If no sources exist, label the claim as speculative and lower confidence.

## 5) Conflict Handling
When sources disagree:
- present both sides (Water)
- state uncertainty
- show how the tie is broken (Fire) using coherence + auditability + accountability

## 6) Provenance Rules (Fork-Safe)
All derivative works must retain:
- NOTICE
- CITATION.cff
- INSTITUTIONAL_AFFILIATION_STATEMENT.md
- ONCHAIN_METADATA.md (if present)
- Canon pointers back to `gcb-canon-core`

## 7) Safety and Non-Investment Framing
- No instructions facilitating wrongdoing or evasion.
- No harassment or hate.
- No ROI/profit framing for tokens.
- Keep content safe and age-appropriate where relevant.

## 8) Validation
If producing JSON artifacts, validate them against the schemas in `/schemas`.

Recommended:
- `schemas/canon-claim.schema.json`
- `schemas/canon-citation.schema.json`