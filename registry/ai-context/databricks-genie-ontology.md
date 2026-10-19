# Databricks Genie Ontology
- Catalogue ID: databricks-genie-ontology
- Category: ai-business-context
- Subtype: inferred-and-curated-agent-context
- Ownership: vendor-led
- Steward: Databricks
- Scope: cross-industry capability; organisation-specific context
- Maturity: Public Preview in inspected documentation
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
Genie Ontology combines governed Unity Catalog semantics with snippets inferred from assets such as metric views, dashboards and SQL queries. Genie One and Genie Code use this shared context.

The documentation describes snippet ranking using origin, usage and freshness, with Unity Catalog permissions and answer citations. These are vendor-described mechanisms, not SIEL-tested accuracy or security results.

This is a business-context capability built around an organisation's assets, not a published industry vocabulary like FIBO. The inspected documentation marks it Public Preview.

Dependencies include Databricks Genie experiences, Unity Catalog and the assets supplying context. Exact workspace configuration, release availability, runtime entitlements, model export rights and context portability were not verified.

## Questions to evaluate in an implementation
- Which definition is retrieved when two authorised departments use the same term differently?
- Can a reviewer inspect, correct and retire inferred context?
- Do citations identify the actual definition and version used?
- What happens after a source definition changes?
Ranking relevance is not, by itself, proof of business correctness. These are SIEL evaluation questions, not observed defects.

## Official sources
- [Official Genie Ontology documentation](https://docs.databricks.com/aws/en/genie/genie-ontology), context categories, ranking and permissions; updated 11 September 2026.
- [Operationalising Genie Ontology](https://www.databricks.com/blog/operationalizing-genie-ontology-your-data-stack), 1 September 2026; vendor guidance, not independent outcome evidence.
Checked 2026-10-19. Product documentation establishes described capability, not implementation success.

## Evidence gap
No customer deployment, benchmark, portability result or maintenance-cost study was independently assessed in this record. Missing evidence is not failure. Apply the [evidence policy](../../docs/evidence-policy.md).
