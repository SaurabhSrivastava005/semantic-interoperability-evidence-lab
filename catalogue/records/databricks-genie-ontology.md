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

## Acceptance questions and difficult cases
| Proposed test | Evidence to retain |
|---|---|
| Finance and Sales define revenue differently | Question scope, authorised candidate definitions, selected snippet and reviewer decision |
| An old dashboard remains popular after a policy change | Asset revisions, retrieval timestamps and time until answers reflect the new policy |
| A user loses access to a source | Before/after retrieval and answers, including cached or conversational context |
| A citation points to an exploratory query | Exact cited content, its approval status and whether the answer treats it as authoritative |

## Industry example and boundaries
Proposed higher-education case: distinguish enrolled students, funded enrolments and course participation. Evaluate the same question across a census date and a funding-rule change. This is a test design, not a reported deployment.

Dependencies include Unity Catalog, the supplying assets and the selected Genie experience. Snippet export, reproducible ranking, version pinning, workspace availability and customer reuse rights were not established by this source check. Do not interpret this as evidence that those capabilities are absent.

## Official sources and evidence status
- [S1: Genie Ontology](https://docs.databricks.com/aws/en/genie/genie-ontology), updated 11 September 2026; checked 20 October 2026.
- [S2: Unity Catalog semantics](https://docs.databricks.com/aws/en/uc-semantics/), updated 11 September 2026; checked 20 October 2026.
- [Operationalising Genie Ontology](https://www.databricks.com/blog/operationalizing-genie-ontology-your-data-stack), retained vendor guidance; not newly rechecked in this pass.

No runtime evaluation or independently reviewed implementation outcome is established. Use the shared [evaluation guide](../../guides/ai-context-evaluation.md) to submit a bounded case.
