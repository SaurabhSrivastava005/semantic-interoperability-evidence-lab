# Microsoft Fabric IQ ontology
- Catalogue ID: microsoft-fabric-iq-ontology
- Category: ai-business-context
- Subtype: data-bound-business-ontology
- Ownership: vendor-led
- Steward: Microsoft
- Scope: cross-industry capability; organisation-specific context
- Maturity: Preview in inspected documentation
- Editorial status: draft; independent reviewer pending
- Prepared by: Codex from official vendor sources
- Source checked: 2026-10-19
- Next review: 2027-04-19
- Regulatory status: not-assessed
- Implementation outcome: not-evaluated
- Licence verification: not-verified for runtime and customer-authored assets
- Source interests: product vendor, not an independent evaluator
- SIEL summary licence: CC BY 4.0; external assets retain their terms

## What it does and what it depends on
Fabric IQ's ontology item defines business entities, properties and relationships with bindings to data. The inspected preview documentation also describes alignment with Power BI semantic models and metrics retaining their source DAX definition.

This is a capability for modelling an organisation's business context, not a supplied universal sector model. Distinguish it from the existing [Power BI semantic-model entry](../analytics/power-bi-semantic-models.md).

Dependencies include Microsoft Fabric items, source bindings and any semantic model supplying metrics. Exact capacity, tenant availability, item versions and runtime entitlements remain to be checked.

The documentation describes a copy-based migration to a new ontology experience. See the [migration boundary](../../exceptions/fabric-iq-ontology-migration.md). No current customer migration or metric correctness was tested.

## Questions to evaluate in an implementation
- Do entity bindings and metric ownership remain traceable after change?
- Are the selected source types supported in the actual tenant?
- What is preserved, changed or excluded by a migration?
- Does an agent use the governed calculation rather than recreate it?
These are evaluation questions; preview documentation is not production evidence.

## Official sources
- [Official ontology overview](https://learn.microsoft.com/en-us/fabric/iq/ontology/overview), Key capabilities, Metric and migration sections; rolling documentation.
Checked 2026-10-19. Product documentation establishes described capability, not implementation success.

## Evidence gap
No customer deployment, benchmark, portability result or maintenance-cost study was independently assessed in this record. Missing evidence is not failure. Apply the [evidence policy](../../docs/evidence-policy.md).
