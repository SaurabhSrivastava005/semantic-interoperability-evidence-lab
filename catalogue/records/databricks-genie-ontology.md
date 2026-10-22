# Databricks Genie Ontology

[Catalogue metadata](../index.yaml) · [Evidence policy](../../guides/evidence-policy.md) · [Comparison](../../guides/ai-context-comparison.md)

## Business problem and architecture
Genie Ontology provides shared business context for Genie One and Genie Code. It combines curated Unity Catalog semantics, including metric views, domains and Pages, with snippets inferred from assets and usage, including dashboards, SQL and Genie Agents. The documentation marks the feature Public Preview. [S1]

The distinction matters when a familiar business expression has several valid meanings. Discovering a frequently used definition and approving a definition for a particular business purpose are different governance decisions.

## Context selection and authority
Databricks describes authority scores based on origin, usage and freshness, permission-gated snippets, conflict resolution and answer citations. These describe the retrieval mechanism; they do not establish that the highest-ranked definition is the correct policy for a particular question. [S1]

SIEL assessment: the unit to inspect is the selected snippet, its originating asset and the task for which it was applied. A citation should be checked for semantic support, rather than counted as proof of correctness.

## Curated lifecycle signals
Unity Catalog semantics documents certification and deprecation as signals for trusted or outdated assets. Metric views are governed SQL objects, while Pages capture business concepts. [S2] This establishes a curated governance mechanism; it does not resolve the separate questions about inspecting and retiring inferred snippets.

## Implementation work to investigate
Start with one bounded domain and identify a business owner for each critical definition. Prepare a source inventory that distinguishes approved metric definitions from exploratory queries and historical dashboards. Document how exceptions apply to business units, time periods and jurisdictions.

Ask the implementation team to demonstrate correction, retirement and propagation of inferred context. Measure the curation and review work, including disagreements between domain owners. These are proposed implementation requirements, not claims about available administration controls.

## Assessment dimensions and evidence
These 24 dimensions apply the shared SIEL framework to this offering and its consuming applications. They are proposed evaluation questions, not verified capabilities, observed defects or exhaustive coverage. Record component responsibility and any justified exclusions using the [shared assessment rules](../../guides/ai-context-evaluation.md#shared-dimension-framework-and-assessment-rules).

### Business meaning

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GEN-01 | Semantic fidelity | Are approved units, metric grain, time boundaries and exclusions preserved in selected snippets and answers? | Approved definition, retrieved snippet and reviewed query/result. |
| GEN-02 | Applicability and exceptions | Does selection distinguish departmental meanings and policy-effective dates rather than merge valid alternatives? | Scoped competing definitions and tasks requiring different answers. |
| GEN-03 | Authority and conflict resolution | When inferred usage conflicts with certified meaning, which definition is selected and why? | Candidate sources, approval/deprecation state and selection evidence where available. |
| GEN-04 | Traceability and revision identity | Can the reviewer identify the source revision supporting a cited snippet and the answer produced from it? | Citation target, source revision, retrieval time and answer trace. |

### Discovery and context quality

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GEN-05 | Asset coverage and discovery | Which required source assets contribute usable context, and which are missing or inaccessible? | In-scope asset inventory, retrieval tasks and labelled omissions. |
| GEN-06 | Relevance and context completeness | Do ranking or context limits exclude necessary qualifications or promote irrelevant popular assets? | Candidate/selected context where inspectable, request and changed answers. |
| GEN-07 | Relationships, identity and mappings | Are entity identifiers and joins in retrieved examples valid for this question's cardinality and dates? | Approved identity/join rules, inferred examples and fan-out tests. |
| GEN-08 | Metadata quality and source-data quality | Can owners distinguish a stale or misleading snippet from incorrect underlying data? | Separate snippet/source checks and reviewed error attribution. |

### Governance and change

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GEN-09 | Freshness and propagation | After a metric, asset or access rule changes, when do snippets and answers reflect it? | Timed source changes, before/after context and cache observations. |
| GEN-10 | Lifecycle and change control | How are curated assets and inferred context reviewed, corrected, retired and recovered after a bad change? | Demonstrated controls, review history and regression results; record unavailable controls. |
| GEN-11 | Uncertainty and missing context | Does Genie clarify ambiguity or missing context instead of presenting an inferred definition as settled policy? | Ambiguous/unanswerable tasks, actual responses and domain review. |
| GEN-12 | Accountability and stewardship effort | Who owns curated definitions, inferred-context disputes and ongoing review across domains? | Named owners, escalation path, resolution time and curation hours. |

### Security and trust boundaries

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GEN-13 | End-to-end authorization | Do source permissions and revocations hold through snippet retrieval, conversation state and generated execution? | User identity, allowed/denied tasks, revocation and execution decisions. |
| GEN-14 | Privacy and information exposure | Can snippets, citations or answer history expose sensitive information to an unintended audience? | Restricted-source cases, displayed payloads and log/cache access review. |
| GEN-15 | Untrusted context and instruction handling | How does the consumer handle instructions embedded in SQL comments, dashboards or other context assets? | Controlled hostile content, selected context and tool/query traces. |
| GEN-16 | Location, retention and use constraints | Do the actual Genie configuration and integrations satisfy processing-location, retention and use requirements? | Deployment/data flow, applicable terms, model settings and retained artefacts. |

### Consumer behaviour and reproducibility

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GEN-17 | Downstream semantic correctness | Does the generated query apply the selected business rule accurately, rather than merely cite it? | Approved logic, selected context, generated SQL and checked result. |
| GEN-18 | Cross-consumer consistency | Do Genie One and Genie Code preserve the same meaning on matched tasks with equivalent authorised context? | Matched tasks, identities, configurations and reviewed output differences. |
| GEN-19 | Auditability and repeatability | Can the team reconstruct an answer after context ranking, source assets or consumer configuration changes? | Permitted context snapshots, revisions, configuration and replay differences. |
| GEN-20 | Failure handling and reliability | What happens when context is unavailable, contradictory or stale, or a source query fails? | Failure cases, fallback disclosure, retries and recovery outcomes. |

### Operations, portability and value

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GEN-21 | Performance and scale | How do retrieval and answer latency behave as assets, users and competing definitions increase? | Representative load, context size, component timings and error rates. |
| GEN-22 | Cost and operational burden | What are setup, inference/query, curation and correction costs per attempted and accepted task? | Dated usage, task counts, owner/reviewer hours and incident effort. |
| GEN-23 | Portability and interoperability | Which governed definitions and inferred context can be reused elsewhere with meaning and rights preserved? | Permitted export/API artefacts, conversion gaps and receiving-consumer tests. |
| GEN-24 | Business value and deployment fit | Does the selected preview/deployment configuration improve a bounded task against the current process? | Availability/support details, held-out tasks, baseline, coverage and reviewed outcomes. |

## Industry example and boundaries
Proposed higher-education case: distinguish enrolled students, funded enrolments and course participation. Evaluate the same question across a census date and a funding-rule change. This is a test design, not a reported deployment.

Dependencies include Unity Catalog, the supplying assets and the selected Genie experience. Snippet export, reproducible ranking, version pinning, workspace availability and customer reuse rights were not established by this source check. Do not interpret this as evidence that those capabilities are absent.

## Official sources and evidence status
- [S1: Genie Ontology](https://docs.databricks.com/aws/en/genie/genie-ontology), updated 11 September 2026; checked 20 October 2026.
- [S2: Unity Catalog semantics](https://docs.databricks.com/aws/en/uc-semantics/), updated 11 September 2026; checked 20 October 2026.
- [Operationalising Genie Ontology](https://www.databricks.com/blog/operationalizing-genie-ontology-your-data-stack), retained vendor guidance; not newly rechecked in this pass.

No runtime evaluation or independently reviewed implementation outcome is established. Use the shared [evaluation guide](../../guides/ai-context-evaluation.md) to submit a bounded case.
