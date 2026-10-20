# Snowflake Semantic Views and Cortex Analyst

[Catalogue metadata](../index.yaml) · [Evidence policy](../../guides/evidence-policy.md) · [Comparison](../../guides/ai-context-comparison.md)

## Business problem and architecture
A Semantic View is a schema-level database object defining logical tables, relationships, facts, dimensions and metrics. SQL/authoring tools manage the definition; Cortex Analyst uses semantic context for natural-language SQL generation. Assess the definition, generated query, execution and displayed answer separately. [S1, S2]

SIEL assessment: executable SQL may still use the wrong business grain, denominator, time boundary or join. Analytical grounding should be judged against an approved calculation, not whether the query runs.

## Evaluation and lifecycle
Snowflake documents evaluations against verified question/SQL pairs, measuring results, regressions and latency. Selected evaluation queries are removed from a temporary semantic-view copy so those examples do not guide generation during that run. Other verified queries remain. [S3]

The same page explains that a metric version pins the judge configuration, not SQL generation; repeated runs may generate different SQL. It also recommends transitioning to Cortex Agents. That recommendation is a vendor direction, not independently established superiority. [S3]

Proposed lifecycle work: version the semantic definition, approved questions, expected results, model settings and evaluation configuration together. Keep a separate set of questions not used to author or tune the view. Review individual failures rather than relying only on a score.

## Documented limits and cost boundary
Cortex Analyst does not itself access previous SQL query results and is scoped to SQL-resolvable questions. Its documentation also warns that model restrictions reduce fallback options. AI-generation charges and warehouse execution charges are separate considerations. These boundaries should not be generalised to every surrounding agent or application. [S2]

See the existing [prior-results exception](../../evidence/exceptions/cortex-analyst-prior-results.md). An application may supply additional state, which requires its own evaluation.

## Acceptance questions and difficult cases
| Proposed test | Evidence to retain |
|---|---|
| Join duplicates a transaction across several related rows | Expected grain, logical relationships, generated SQL and result comparison |
| A ratio is requested at a different aggregation level | Approved numerator/denominator and aggregate result |
| A user asks about the second row of an earlier answer | Application state supplied, exact follow-up request and selected entity |
| An account restricts available models | Configuration, generation/evaluation failure and recovery behaviour |
| Semantic metadata is shared or exported | Definition, receiving environment and behaviour/rights review |

## Industry example and boundaries
Proposed retail case: calculate net sales by region with returns, discounts and currency conversion. Include cases that distinguish transaction date from posting date. This is a test specification, not evidence of adoption or success.

Dependencies include source tables, semantic definitions, access roles, compute and available AI models. Do not assign one maturity label to Semantic Views, Analyst, Agents and evaluation tooling collectively. Exported metadata does not by itself establish portable execution or redistribution rights.

## Official sources and evidence status
- [S1: Semantic Views overview](https://docs.snowflake.com/en/user-guide/views-semantic/overview).
- [S2: Cortex Analyst](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-analyst).
- [S3: Cortex Analyst evaluations](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-analyst-evaluations).

Checked 20 October 2026. No SIEL runtime evaluation or independently reviewed implementation outcome is established.
