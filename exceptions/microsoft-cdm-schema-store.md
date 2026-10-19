# Microsoft CDM: Schema Store dependency and SDK migration
- ID: exception-microsoft-cdm-schema-store
- Status: draft; independent review pending
- Prepared by: Codex
- Source checked: 2026-10-19
- Next review: 2027-04-19
- Industry: cross-industry
- Cause category: dependency lifecycle and version mismatch
- Evidence type: vendor maintenance notice, not observed customer failure
- Summary licence: CC BY 4.0; external source terms remain applicable

## Documented boundary
Microsoft's README announces a Schema Store shutdown by the end of March 2024 and warns that services using SDK releases before 1.7.1 may fail when that dependency is unavailable.

From SDK 1.7.1, foundational definitions are bundled. Application schemas are not included in that bundle; projects depending on them must package and reference them separately.

## Response and limits
The vendor directs users to upgrade and manage additional schemas. SIEL has not tested this migration or independently confirmed the shutdown's operational effects. Customer incident counts, costs and residual issues are unknown.

Do not label this as proof that CDM generally fails. It illustrates why a model's deployment dependencies and lifecycle belong in the catalogue.

## Source
[Microsoft CDM README](https://github.com/microsoft/CDM/blob/master/README.md), Important Notice; inspected blob 6475a54ac7ab8391e6089aa47a66b194e329e6ba.

[Related model](../registry/vendors/microsoft-cdm.md).
