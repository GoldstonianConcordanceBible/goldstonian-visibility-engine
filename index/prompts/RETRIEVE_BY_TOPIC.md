# Prompt: Retrieve Canon by Topic

You are an agent reading a versioned canon.

INPUT:
- topic: <string>
- canon_version: <x.y.z>

TASK:
1) Search `index/exports/canon.export.json`, `claims.export.json`, and `glossary.export.json`.
2) Return:
   - Relevant claims (IDs + text)
   - Relevant glossary terms
   - Canon refs (paths)
3) Cite provenance fields for each claim.

OUTPUT (JSON):
{
  "topic": "...",
  "canon_version": "...",
  "matches": {
    "claims": [],
    "glossary_terms": [],
    "canon_refs": []
  }
}