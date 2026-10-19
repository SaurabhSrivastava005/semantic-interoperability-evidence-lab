# Repository Structure
| Location | Purpose |
|---|---|
| registry/ | Starter YAML catalogue and individual standard profiles |
| docs/industries/ | Eight industry entry points and existing landscapes |
| use-cases/ | Business problems and links to relevant standards |
| implementations/ | Sourced, bounded implementation outcomes |
| exceptions/ | Context differences, limitations and workarounds |
| templates/ | Reusable editorial record formats |
| docs/evidence-policy.md | Outcome, source and review rules |
| decision-records/ | Material editorial decisions |
| archive/ | Superseded platform and research proposals |

## Linking rules
Use stable IDs in records and relative links between files. A use-case guide links to standard profiles or official sources; implementation cases link to the use case, standards and exceptions. Exceptions link back to affected cases. Industry guides act as entry points rather than duplicate record contents.

## Publication workflow
Create a Markdown record from a template, submit through a pull request, apply the evidence policy and record reviewer approval. Empty collections are identified openly. Add a record only when useful content and authorised sources are available.

## Structure review
The earlier design mixed a knowledge catalogue with a platform product and benchmark programme. The current structure separates discovery, experience and exceptions without requiring users to install software. Existing industry paths are retained to preserve navigation. Earlier proposals are archived and do not count as implementation cases.

The YAML catalogue remains discovery metadata. Individual profiles carry editorial assessment and source details; when both exist, keep the same stable standard ID and link them.

## Catalogue subcollections
- `registry/ontologies/`: domain ontologies, vocabularies and industry information models.
- `registry/analytics/`: analytical semantic modelling systems.
- `registry/knowledge-graphs/`: published graph datasets.
- `registry/technologies/`: modelling languages and execution platforms.
- `registry/vendors/`: existing vendor-owned model profiles.

An asset has one canonical profile and catalogue ID even when multiple browse pages link it. LookML remains in the vendor directory and is cross-linked from the semantic catalogue.

## AI business context
`registry/ai-context/` holds vendor capability profiles. `docs/ai-context-evaluation.md` provides evidence-collection questions. The category is distinct from domain ontologies and does not require SIEL to implement a platform or run a benchmark.
