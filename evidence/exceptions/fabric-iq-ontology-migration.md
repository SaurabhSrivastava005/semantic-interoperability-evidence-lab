---
id: exception-fabric-iq-ontology-migration
record_type: exception
editorial_status: draft
prepared_by: Codex from cited sources
independent_reviewer: pending
source_checked_on: '2026-10-19'
next_review: '2027-04-19'
catalogue_ids:
- microsoft-fabric-iq-ontology
finding_type: vendor-migration-boundary
provenance_notes:
  Cause category: feature lifecycle and migration
  Evidence type: vendor documentation, not an observed failure
---
# Fabric IQ ontology: migration between preview experiences

## Documented boundary
Microsoft's inspected ontology preview overview describes a migration by creating a copy in the new experience while preserving the original item. It describes preservation of supported definitions.

## Implication
Treat the copy as a separate item and check downstream bindings and consumers. Do not assume that every preview configuration transfers unchanged. SIEL has not executed the migration, measured effort or established any customer failure.

Source: [official ontology overview](https://learn.microsoft.com/en-us/fabric/iq/ontology/overview), migration guidance.

[Related profile](../../catalogue/records/microsoft-fabric-iq-ontology.md). Exact tenant availability and migration behaviour need version-specific validation.
