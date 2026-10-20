---
id: exception-palantir-action-write-controls
record_type: exception
editorial_status: draft
prepared_by: Codex from cited sources
independent_reviewer: pending
source_checked_on: '2026-10-20'
next_review: '2027-04-20'
catalogue_ids:
- palantir-ontology
finding_type: vendor-security-boundary
provenance_notes:
  Evidence type: vendor documentation, not a customer incident or reproduced failure
---
# Palantir actions: read controls and write protection

## Documented boundary
The action-permissions guide distinguishes read-time row/column controls from protection on action writes. It directs authors to use marking or Classification-based Access Control for downstream data protection. This is a configuration boundary, not evidence of a vulnerability.

## Evidence to request
Inspect source access, submission criteria, read/write authorizations and resulting data protection together. Retain denied and permitted action examples. SIEL has not tested a deployment or observed a data exposure.

Source: [Action permissions](https://www.palantir.com/docs/foundry/action-types/permissions), Apply action and Read-time enforcement only.

[Related profile](../../catalogue/records/palantir-ontology.md). Frequency and business impact remain unassessed.
