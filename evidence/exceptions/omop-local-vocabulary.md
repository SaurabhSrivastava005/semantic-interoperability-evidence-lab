---
id: exception-omop-local-vocabulary
record_type: exception
editorial_status: draft
prepared_by: Saurabh/Codex from cited sources
independent_reviewer: pending
source_checked_on: '2026-10-19'
next_review: '2027-04-19'
catalogue_ids:
- omop-cdm
finding_type: reported-implementation-limitation
provenance_notes:
  Industry: Healthcare
  Jurisdiction: European network
  Conflicts: no author interests supplied; source affiliations must be considered
---
# OMOP: local vocabulary mapping needs site-specific review

## Finding
In the [EHDEN case](../implementations/healthcare-ehden-omop.md), initial quality runs addressed conformance issues; later runs addressed more complex local vocabulary mappings. Default thresholds were subsequently adapted to source-specific conditions.

- Cause: semantic ambiguity and source variation; not a blanket model defect.
- Consequence: common structure does not complete terminology harmonisation.
- Reported response: iterative mapping, quality checks and inspection.
- Cost and residual error rate: not established.
- Resolution: reported as part of the programme; not independently retested.
- Version boundary: per-site versions not established.

## Source
[Blacketer et al., 2025](https://www.jmir.org/2025/1/e74119/), Methods: Data Quality. Checked 2026-10-19. This is a reported implementation limitation, not a claim that OMOP fails generally.

## Related standard
[OMOP CDM](../../catalogue/records/omop-cdm.md).
