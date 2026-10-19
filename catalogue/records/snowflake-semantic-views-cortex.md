# Snowflake Semantic Views and Cortex Analyst

[Catalogue metadata](../index.yaml) · [Evidence policy](../../guides/evidence-policy.md)

## What it does and what it depends on
Semantic Views define logical business tables, relationships, facts, dimensions and metrics. Cortex Analyst uses semantic context to generate SQL from natural-language questions.

This is an analytical grounding capability. It is not equivalent in scope to an operational ontology with business actions. The semantic view, generated query, executed result and conversational state are separate things to assess.

Dependencies include Snowflake objects, source data, access privileges and supported model configurations. Exact release, region, runtime entitlement and semantic-asset redistribution rights remain unverified.

Cortex Analyst documents a limitation on referring to earlier SQL result rows in follow-up questions. See the [multi-turn boundary](../../evidence/exceptions/cortex-analyst-prior-results.md). No independently measured answer accuracy or customer outcome is established here.

## Questions to evaluate in an implementation
- Does generated SQL implement the intended metric, grain and filters?
- Do held-out questions and paraphrases return equivalent results?
- Are verified queries representative of actual use?
- Are follow-up questions tested with the surrounding application's result-handling logic?
A successful SQL execution is insufficient evidence of correct business meaning.

## Official sources
- [Semantic Views overview](https://docs.snowflake.com/en/user-guide/views-semantic/overview), Understanding semantic views.
- [Cortex Analyst](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-analyst), semantic views, evaluation and multi-turn limitations; rolling vendor documentation.
Checked 2026-10-19. Product documentation establishes described capability, not implementation success.

## Related records
- [cortex analyst prior results](../../evidence/exceptions/cortex-analyst-prior-results.md)
