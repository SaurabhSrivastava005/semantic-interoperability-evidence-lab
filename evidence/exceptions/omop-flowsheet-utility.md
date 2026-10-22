---
id: exception-omop-flowsheet-utility
record_type: exception
editorial_status: draft
prepared_by: Saurabh/Codex from cited sources
independent_reviewer: pending
source_checked_on: '2026-10-19'
next_review: '2027-04-19'
catalogue_ids:
- omop-cdm
finding_type: reported-implementation-tradeoff
provenance_notes:
  Industry: Healthcare
  Jurisdiction: Study-specific
  Conflicts: no author interests supplied; source affiliations must be considered
---
# OMOP flowsheets: loading data does not ensure analytical utility

## Finding
The [flowsheet study](../implementations/healthcare-flowsheet-omop.md) reports limited utility from its simpler integration approach and greater utility after more demanding terminology mapping.

- Cause category: semantic mapping approach.
- Diagnosis: authors' comparison, not an independently reproduced result.
- Workaround: reported controlled-vocabulary mapping.
- Cost: increased effort reported; no amount established here.
- Versions and remaining errors: not established from the inspected abstract.
- User implication: define intended analyses before choosing a mapping shortcut.

## Source
[Seto et al., 2021](https://arxiv.org/abs/2109.08235), Abstract; checked 2026-10-19. This is a bounded tradeoff, not evidence that the entire model is unsuccessful.

[Standard profile](../../catalogue/records/omop-cdm.md).
