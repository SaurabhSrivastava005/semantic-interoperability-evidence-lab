# Fabric IQ ontology: migration between preview experiences
- ID: exception-fabric-iq-ontology-migration
- Status: draft; independent review pending
- Prepared by: Codex
- Source checked: 2026-10-19
- Next review: 2027-04-19
- Cause category: feature lifecycle and migration
- Evidence type: vendor documentation, not an observed failure
- SIEL summary licence: CC BY 4.0; external terms separate

## Documented boundary
Microsoft's inspected ontology preview overview describes a migration by creating a copy in the new experience while preserving the original item. It describes preservation of supported definitions.

## Implication
Treat the copy as a separate item and check downstream bindings and consumers. Do not assume that every preview configuration transfers unchanged. SIEL has not executed the migration, measured effort or established any customer failure.

Source: [official ontology overview](https://learn.microsoft.com/en-us/fabric/iq/ontology/overview), migration guidance.

[Related profile](../registry/ai-context/microsoft-fabric-iq-ontology.md). Exact tenant availability and migration behaviour need version-specific validation.
