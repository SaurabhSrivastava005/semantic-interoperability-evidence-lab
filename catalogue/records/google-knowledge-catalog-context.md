# Google Knowledge Catalog data context

[Catalogue metadata](../index.yaml) · [Evidence policy](../../guides/evidence-policy.md) · [Comparison](../../guides/ai-context-comparison.md)

## Business problem and architecture
Knowledge Catalog combines technical metadata, business descriptions, relationships and trust signals for context consumers. A service providing metadata and a service consuming context play different roles; a connector does not establish automatic downstream use. This is distinct from [LookML modelling](google-looker-lookml.md). [S1]

The central implementation question is what useful context reaches an application at the moment it selects an asset or generates a query.

## Retrieval, integration and permissions
The documented sequence is asset discovery, a LookupContext request, a formatted metadata response, and consumer use of that response. REST and MCP integrations are described. Context can include schemas, business terms, operational relationships, profiles and quality outputs. The guide requires API enablement and suitable IAM permissions; it documents permission-filtered responses, including an empty response when access is missing. [S2]

Requests support up to ten resources. The context budget is expressed in characters; requesting all schema fields can override that budget. [S2]

SIEL assessment: measure retrieval separately from the agent's interpretation. An application can receive the right definition and still construct the wrong query. A character budget also should not be treated as a guaranteed model-token limit.

## Governance and maintenance work
Proposed implementation work: assign owners to glossary terms, source descriptions and agent guidelines; record which metadata is curated versus inferred; define refresh expectations and retirement rules. Treat historical join usage as evidence to inspect, rather than proof that a join is appropriate for every business question.

Keep retrieval request, identity, response and downstream tool call together when investigating errors. Check whether cached context remains appropriate after permissions or definitions change. These are evidence requirements, not assertions about unverified product controls.

## Acceptance questions and difficult cases
| Proposed test | Evidence to retain |
|---|---|
| Relevant assets have competing glossary definitions | Discovery results, requested assets, returned definitions and chosen scope |
| A small budget excludes an important qualification | Request options, exact response and changed answer |
| Metadata is readable but source data is restricted | Retrieval identity, query identity and source authorization decision |
| A frequent historical join is invalid for this task | Returned relationship, approved join logic and generated query |
| Two agents receive the same context | Exact response and each agent's independently reviewed output |

## Industry example and boundaries
Proposed government case: discover an approved service-performance dataset and interpret its eligibility and reporting-period definitions. Evaluate discovery, semantic interpretation and lawful source access separately. This is an illustrative scenario, not an implemented case.

The docs' content footer specifies CC BY 4.0 and Apache 2.0 for code samples, subject to exceptions. That notice does not license the hosted service or determine rights in customer metadata. [S1] Runtime rights, region-specific availability, cache invalidation and complete context portability were not established.

## Official sources and evidence status
- [S1: About data context](https://docs.cloud.google.com/knowledge-catalog/docs/about-context), updated 13 October 2026.
- [S2: Retrieve context for data assets](https://docs.cloud.google.com/knowledge-catalog/docs/retrieve-data-context), updated 15 October 2026.

Checked 20 October 2026. No SIEL measurement of cross-agent consistency, answer quality or customer outcome is established.
