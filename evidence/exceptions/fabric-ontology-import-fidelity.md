---
id: exception-fabric-ontology-import-fidelity
record_type: exception
editorial_status: draft
prepared_by: Codex from cited sources
independent_reviewer: pending
source_checked_on: '2026-10-20'
next_review: '2027-04-20'
catalogue_ids:
- microsoft-fabric-iq-ontology
finding_type: vendor-interoperability-boundary
provenance_notes:
  Evidence type: vendor documentation, not a customer incident or reproduced failure
---
# Fabric ontology: import conversion can alter definitions

## Documented boundary
The preview import guide requires an empty ontology item. Its import summary distinguishes preserved, adjusted and unsupported content, including retention of only the first parent for multiple inheritance. Format acceptance therefore does not establish lossless semantic conversion.

## Evidence to request
Retain the original file, import summary and resulting definition. Compare the answers to relevant domain questions before and after conversion. SIEL has not run an import or measured semantic loss.

Source: [Import and export ontologies](https://learn.microsoft.com/en-us/fabric/iq/ontology/how-to-import-export), Review import summary.

[Related profile](../../catalogue/records/microsoft-fabric-iq-ontology.md). This is a documented conversion limit, not an implementation failure report.
