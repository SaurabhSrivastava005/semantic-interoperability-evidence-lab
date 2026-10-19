---
id: exception-ifc-tool-interpretation
record_type: exception
editorial_status: draft
prepared_by: Codex from cited sources
independent_reviewer: pending
source_checked_on: '2026-10-19'
next_review: '2027-04-19'
catalogue_ids:
- ifc
finding_type: reported-implementation-limitation
provenance_notes:
  Industry: Real estate and construction
  Jurisdiction: GeoBIM benchmark scope
  Conflicts: no author interests supplied; source affiliations must be considered
---
# IFC: interpretation and export vary by software workflow

## Finding
The [GeoBIM case](../implementations/construction-geobim-ifc.md) identifies inconsistent handling of standardised building data. The authors recommend clearer controls and warn against silently filling undefined information with import/export defaults.

- Cause category: implementation differences and model complexity; relative causation is unresolved.
- Affected versions: tested IFC2x3 and IFC4 datasets.
- Response: proposed explicit settings and validation; not a SIEL-tested fix.
- Cost, universal workaround and current-tool status: not established.
- Implication: test the actual exporter, importer and required information.

## Source
[Noardo et al., Part I](https://arxiv.org/html/2007.10951v2), sections 5.1 and 6; checked 2026-10-19.

[Standard profile](../../catalogue/records/ifc.md).
