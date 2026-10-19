# IFC: interpretation and export vary by software workflow
- ID: exception-ifc-tool-interpretation
- Editorial status: draft
- Prepared by: Codex, from public sources
- Independent reviewer: pending
- Industry: Real estate and construction
- Jurisdiction: GeoBIM benchmark scope
- Source check: 2026-10-19
- Next review due: 2027-04-19
- Conflicts: no author interests supplied; source affiliations must be considered
- Licence: CC BY 4.0 for this original summary; linked sources retain their terms

## Finding
The [GeoBIM case](../implementations/construction-geobim-ifc.md) identifies inconsistent handling of standardised building data. The authors recommend clearer controls and warn against silently filling undefined information with import/export defaults.

- Cause category: implementation differences and model complexity; relative causation is unresolved.
- Affected versions: tested IFC2x3 and IFC4 datasets.
- Response: proposed explicit settings and validation; not a SIEL-tested fix.
- Cost, universal workaround and current-tool status: not established.
- Implication: test the actual exporter, importer and required information.

## Source
[Noardo et al., Part I](https://arxiv.org/html/2007.10951v2), sections 5.1 and 6; checked 2026-10-19.

[Standard profile](../registry/ifc.md).
