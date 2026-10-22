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

## Assessment dimensions and evidence
These 24 dimensions apply the shared SIEL framework to this offering and its consuming applications. They are proposed evaluation questions, not verified capabilities, observed defects or exhaustive coverage. Record component responsibility and any justified exclusions using the [shared assessment rules](../../guides/ai-context-evaluation.md#shared-dimension-framework-and-assessment-rules).

### Business meaning

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| SNF-01 | Semantic fidelity | Do facts, dimensions, metric grain, units and aggregation rules encode the approved business meaning? | Approved definitions, semantic-view definition and expected results. |
| SNF-02 | Applicability and exceptions | Are period, currency, jurisdiction and departmental metric variants selected for the correct scope? | Variant definitions, scope rules and contrasting analytical cases. |
| SNF-03 | Authority and conflict resolution | Who approves a metric or verified query, and how are conflicting definitions and examples resolved? | Ownership/approval records, conflicting definitions and resolution rationale. |
| SNF-04 | Traceability and revision identity | Can an answer be traced to the semantic-view revision, generated SQL and source-data state? | Definition revision, request/query identifiers, execution time and permitted source snapshot. |

### Discovery and context quality

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| SNF-05 | Asset coverage and discovery | Which required tables, metrics, question types and integrations are covered, and which remain unsupported? | In-scope inventory, attempted-task set and explicit exclusions. |
| SNF-06 | Relevance and context completeness | Does the consumer receive enough semantic context without confusing similar views, dimensions or examples? | Chosen view/context, competing candidates where inspectable and reviewed outputs. |
| SNF-07 | Relationships, identity and mappings | Do logical relationships and joins preserve intended grain and cardinality, including many-to-many cases? | Approved joins, duplication tests and reconciled aggregate results. |
| SNF-08 | Metadata quality and source-data quality | Can semantic-definition or example defects be distinguished from missing, late or incorrect source data? | Separate definition/data checks and reviewed discrepancy attribution. |

### Governance and change

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| SNF-09 | Freshness and propagation | When data, metric definitions or verified queries change, when do consumers and evaluations reflect the change? | Timed updates, definition/request revisions and before/after results. |
| SNF-10 | Lifecycle and change control | How are semantic-view and evaluation changes reviewed, deployed and recovered when regressions appear? | Versioned definitions/tests, review history, regressions and recovery evidence. |
| SNF-11 | Uncertainty and missing context | Does the consumer clarify ambiguous terms and handle questions that cannot be answered from available context? | Ambiguous/unanswerable questions, abstentions and reviewer assessment. |
| SNF-12 | Accountability and stewardship effort | Who owns metric definitions, verified-query quality, evaluation review and application conversation state? | Role assignments, failure queues, resolution times and maintenance hours. |

### Security and trust boundaries

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| SNF-13 | End-to-end authorization | Are generation, evaluation and SQL execution performed under the intended roles and source permissions? | Identity/role chain, permitted/denied queries, revocation and actual result access. |
| SNF-14 | Privacy and information exposure | Can semantic metadata, example SQL, results, prompts or logs expose restricted business information? | Restricted-user cases and review of supplied context, outputs, logs and caches. |
| SNF-15 | Untrusted context and instruction handling | How does the consumer handle malicious instructions in descriptions, example questions or other supplied context? | Controlled adversarial content, application policy and actual generated/executed operations. |
| SNF-16 | Location, retention and use constraints | Do model routing, cross-region settings, query/result retention and application hosting meet requirements? | Actual configuration, data flows, retention and relevant service terms. |

### Consumer behaviour and reproducibility

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| SNF-17 | Downstream semantic correctness | Does generated SQL produce the approved result, including filters, ratios, grain and follow-up references? | Expected SQL/results, generated SQL, prior-result state supplied and reconciled output. |
| SNF-18 | Cross-consumer consistency | Do Analyst, Agents or other consuming applications preserve equivalent metrics on matched tasks? | Exact consumer/version/configuration, matched tasks and reviewed result differences. |
| SNF-19 | Auditability and repeatability | Can evaluation changes be attributed to definition, source data, generation or judge changes? | Pinned evaluation settings, permitted data revisions, generated SQL and repeated-run differences. |
| SNF-20 | Failure handling and reliability | How are generation failures, unavailable models, execution errors and missing conversation state handled? | Controlled failures, application responses, retries/fallbacks and recovery outcomes. |

### Operations, portability and value

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| SNF-21 | Performance and scale | Does the generation-plus-execution workflow meet targets at realistic question complexity and concurrency? | Workload shape, generation/execution timings, warehouse load and failure rates. |
| SNF-22 | Cost and operational burden | What is the total cost per accepted answer, including generation, execution, evaluation and human review? | Dated AI/warehouse usage, evaluation cost, task counts and author/reviewer effort. |
| SNF-23 | Portability and interoperability | Which definitions, joins, metrics and verified queries retain meaning in another consumer or environment? | Permitted definition/export artefacts, receiving-system results, conversion gaps and rights. |
| SNF-24 | Business value and deployment fit | Does the selected feature combination improve analytical work against an approved baseline? | Feature/version/region details, held-out questions, coverage, correctness and review effort. |

## Industry example and boundaries
Proposed retail case: calculate net sales by region with returns, discounts and currency conversion. Include cases that distinguish transaction date from posting date. This is a test specification, not evidence of adoption or success.

Dependencies include source tables, semantic definitions, access roles, compute and available AI models. Do not assign one maturity label to Semantic Views, Analyst, Agents and evaluation tooling collectively. Exported metadata does not by itself establish portable execution or redistribution rights.

## Official sources and evidence status
- [S1: Semantic Views overview](https://docs.snowflake.com/en/user-guide/views-semantic/overview).
- [S2: Cortex Analyst](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-analyst).
- [S3: Cortex Analyst evaluations](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-analyst-evaluations).

Checked 20 October 2026. No SIEL runtime evaluation or independently reviewed implementation outcome is established.
