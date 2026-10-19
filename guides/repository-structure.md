# Repository Structure and Maintenance

| Location | Single responsibility |
|---|---|
| catalogue/index.yaml | Canonical metadata and evidence links for each catalogue ID |
| catalogue/records/ | One narrative and source record per catalogue ID |
| catalogue/README.md, by-ownership.md | Generated browse views; do not duplicate descriptions here |
| catalogue/discovery-backlog.md | Deduplicated leads not yet promoted into the catalogue |
| industries/index.yaml | Canonical industry membership and case references |
| industries/*.md | Industry context, business questions and links to canonical records |
| use-cases/ | Bounded business questions and selection guidance |
| evidence/implementations/ | Sourced implementation results with YAML front matter |
| evidence/exceptions/ | Reported limitations and documented boundaries with finding types |
| guides/ | Shared classification, evidence and evaluation guidance |
| templates/ | Record formats for contributors |
| decision-records/ | Material editorial decisions |
| archive/ | Historical proposals and superseded batch notes |
| scripts/ | Local content maintenance, not a product platform |

## Source of truth

Update a catalogue entry's structured metadata in index.yaml, and its source-specific explanation in its canonical profile. Do not repeat the same licence conclusion or description in industry and category pages. Link to the profile instead. Stable IDs do not change when display titles change.

Evidence front matter identifies catalogue IDs and finding types. Index metadata links back to that evidence. Catalogue metadata contains discovery status; outcomes remain scoped to case records.

The discovery backlog preserves additional official-source leads from the old landscapes without presenting them as reviewed catalogue entries. An inherited description is not a new source check.

## Regenerate and validate

Run from the repository root:

```bash
python -m pip install -r requirements.txt
python scripts/maintain_catalogue.py --write
python scripts/maintain_catalogue.py
```

Checks cover duplicate YAML keys and IDs, one profile per entry, required fields, evidence references, local Markdown targets and stale generated views. They do not verify external URL availability, licences, semantic correctness or business outcomes. External sources still need human review. This command is a content-integrity check, not a conformance runner.

## History and moved paths

Current guidance supersedes appended batch summaries. Historical notes are retained in the archive; git history preserves earlier paths and wording. See [path migration](path-migration.md) for moved content. Links from outside GitHub to removed paths will need updating; no duplicate redirect files are maintained.
