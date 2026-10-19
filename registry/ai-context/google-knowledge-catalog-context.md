# Google Knowledge Catalog data context
- Catalogue ID: google-knowledge-catalog-context
- Category: ai-business-context
- Subtype: catalogue-context-retrieval
- Ownership: vendor-led
- Steward: Google Cloud
- Scope: cross-industry capability; organisation-specific context
- Maturity: Not established for every API or integration; verify selected feature
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
Google describes data context as a combination of technical metadata, business semantics, relationships and trust signals used by people and agents. Documentation includes glossary definitions and context retrieval mechanisms.

This is catalogue-based business context, distinct from the existing [LookML modelling entry](../vendors/google-looker-lookml.md). A metadata provider and an application consuming that metadata are different roles; do not assume every connected application uses the context automatically.

Dependencies include configured catalogue assets, metadata sources, permissions and the selected consumer/API integration. Exact feature availability, release status, runtime entitlement, export rights and third-party source conditions were not established.

Vendor statements about answer quality are not treated as independently measured guarantees.

## Questions to evaluate in an implementation
- Which definitions and source revisions reach the consuming agent?
- Are stale metadata and conflicting glossary entries visible?
- Are permissions respected end to end by the chosen integration?
- Does retrieved context improve a held-out task against an explicit baseline?
No cross-agent consistency or business outcome was evaluated by SIEL.

## Official sources
- [About data context](https://docs.cloud.google.com/knowledge-catalog/docs/about-context), semantic metadata, context consumers and retrieval mechanisms.
- [Retrieve context for data assets](https://docs.cloud.google.com/knowledge-catalog/docs/retrieve-data-context), context retrieval workflow; rolling vendor documentation.
Checked 2026-10-19. Product documentation establishes described capability, not implementation success.

## Evidence gap
No customer deployment, benchmark, portability result or maintenance-cost study was independently assessed in this record. Missing evidence is not failure. Apply the [evidence policy](../../docs/evidence-policy.md).
