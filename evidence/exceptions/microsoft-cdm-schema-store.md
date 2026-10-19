---
id: exception-microsoft-cdm-schema-store
record_type: exception
editorial_status: draft
prepared_by: Codex from cited sources
independent_reviewer: pending
source_checked_on: '2026-10-19'
next_review: '2027-04-19'
catalogue_ids:
- microsoft-cdm
finding_type: vendor-maintenance-notice
provenance_notes:
  Industry: cross-industry
  Cause category: dependency lifecycle and version mismatch
  Evidence type: vendor maintenance notice, not observed customer failure
---
# Microsoft CDM: Schema Store dependency and SDK migration

## Documented boundary
Microsoft's README announces a Schema Store shutdown by the end of March 2024 and warns that services using SDK releases before 1.7.1 may fail when that dependency is unavailable.

From SDK 1.7.1, foundational definitions are bundled. Application schemas are not included in that bundle; projects depending on them must package and reference them separately.

## Response and limits
The vendor directs users to upgrade and manage additional schemas. SIEL has not tested this migration or independently confirmed the shutdown's operational effects. Customer incident counts, costs and residual issues are unknown.

Do not label this as proof that CDM generally fails. It illustrates why a model's deployment dependencies and lifecycle belong in the catalogue.

## Source
[Microsoft CDM README](https://github.com/microsoft/CDM/blob/master/README.md), Important Notice; inspected blob 6475a54ac7ab8391e6089aa47a66b194e329e6ba.

[Related model](../../catalogue/records/microsoft-cdm.md).
