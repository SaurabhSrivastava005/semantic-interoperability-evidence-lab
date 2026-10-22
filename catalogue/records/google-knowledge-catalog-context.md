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

## Assessment dimensions and evidence
These 24 dimensions are SIEL's proposed assessment framework for a Knowledge Catalog implementation and its consuming applications. They are questions to investigate, not verified Google capabilities, observed defects or a claim of exhaustive coverage. The deployment owner should add industry-specific obligations and mark exclusions with reasons.

### Business meaning

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GKC-01 | Semantic fidelity | Do definitions, units, grain, time basis and exclusions retain their meaning from source through retrieved context to the agent's answer? | Approved definitions, exact context and reviewed answer/query comparison. |
| GKC-02 | Applicability and exceptions | Does the consumer select the definition valid for the industry, business unit, jurisdiction and effective date, and preserve legitimate alternatives? | Competing definitions, scope rules and cases requiring different correct answers. |
| GKC-03 | Authority and conflict resolution | Can the reviewer distinguish approved, inferred and deprecated definitions, identify the accountable owner, and explain how a conflict is resolved? | Approval/ownership records, conflicting entries and selected authority with rationale. |
| GKC-04 | Traceability and revision identity | Which definitions and source revisions reach the consuming agent, and can its answer be traced to the exact context used? | Source and definition identifiers/revisions, retrieval timestamp and linked request/response/answer records. |

### Discovery and context quality

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GKC-05 | Asset coverage and discovery | Which required asset types, domains and sources are represented, and can the consumer find relevant authorised assets without silently omitting them? | In-scope asset inventory, labelled discovery tasks, missing assets and recall/precision against that inventory. |
| GKC-06 | Relevance and context completeness | Does selection or budget reduction omit qualifiers, relationships or exceptions needed for the task, or include distracting material? | Full reference context, request options, actual payload, omissions and resulting answer differences. |
| GKC-07 | Relationships, identity and mappings | Do identifiers, entity mappings and join paths represent the intended business relationship, including cardinality and historical validity? | Approved mappings and joins, duplicate/missing-identity cases, fan-out cases and checked results. |
| GKC-08 | Metadata quality and source-data quality | Are stale metadata and conflicting glossary entries visible, and are metadata defects distinguished from incomplete or incorrect source data? | Separate metadata/data checks, observed defects, quality-signal scope and incident classification. |

### Governance and change

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GKC-09 | Freshness and propagation | How long do source, glossary and policy changes take to reach retrieval, caches and consuming applications? | Timed changes, before/after payloads, cache observations and agreed freshness targets. |
| GKC-10 | Lifecycle and change control | Can owners review, approve, deprecate and remove context, assess downstream impact and recover from an incorrect change? | Change/approval history, affected consumers, deletion/deprecation tests and recovery evidence. |
| GKC-11 | Uncertainty and missing context | Can the application distinguish ambiguity, missing metadata, denied access and retrieval failure, then clarify, abstain or escalate appropriately? | Cases for each condition, actual responses and reviewed decision/escalation behaviour. |
| GKC-12 | Accountability and stewardship effort | Who resolves disputed meanings and maintains each source, mapping and integration, and what happens when ownership changes? | Named roles, unresolved-item queues, handover records, resolution times and observed maintenance hours. |

### Security and trust boundaries

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GKC-13 | End-to-end authorization | Are permissions respected across discovery, retrieval, caches, agent identity, source execution and any downstream tool or action? | User/service-account identity chain, allowed/denied cases, revocation tests and source/tool decisions. |
| GKC-14 | Privacy and information exposure | Can descriptions, profiles, samples, lineage, prompts, logs or caches reveal information the intended user should not receive? | Field-level exposure review, restricted-user tests, log/cache access and retention/deletion evidence. |
| GKC-15 | Untrusted context and instruction handling | How does the consumer handle misleading or malicious instructions embedded in descriptions, examples or other retrieved metadata? | Controlled adversarial metadata, consumer policy, tool-call traces and reviewed containment outcomes. |
| GKC-16 | Location, retention and use constraints | Where is context processed and retained, and do the selected integrations honour the organisation's location, retention and permitted-use requirements? | Deployment/data-flow inventory, configured retention, applicable terms and evidence of required controls. |

### Consumer behaviour and reproducibility

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GKC-17 | Downstream semantic correctness | Does the consumer actually apply the supplied definition when generating a query, explanation or tool call? | Approved interpretation, exact context, generated operation and reviewed result/final state. |
| GKC-18 | Cross-consumer consistency | When applications or agents receive equivalent context and identity scope, do they preserve the same business meaning and explain divergences? | Matched tasks and payloads, consumer/model configurations and domain-reviewed differences. |
| GKC-19 | Auditability and repeatability | Can an investigator reconstruct a result after metadata, source data, model or application versions have changed? | Linked traces, permitted snapshots/revisions, configuration versions and replay differences. |
| GKC-20 | Failure handling and reliability | What happens during an empty, partial, delayed or failed retrieval, and can retries or fallback produce an unlabelled answer from stale context? | Injected failure cases, error/retry records, fallback disclosures and recovery behaviour. |

### Operations, portability and value

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| GKC-21 | Performance and scale | Does the complete workflow meet agreed latency and availability targets at realistic asset counts, context sizes and concurrent load? | Workload shape, p50/p95 latency, error rates, quota behaviour and component timings. |
| GKC-22 | Cost and operational burden | What is the cost per attempted and accepted task, including retrieval, model/query execution, integration and human review? | Dated usage/cost records, accepted/failed task counts, setup effort and ongoing review hours. |
| GKC-23 | Portability and interoperability | Which definitions, identifiers, relationships and provenance can be reused by another consumer or environment with meaning and rights preserved? | Permitted export/API artefacts, receiving-system comparison, conversion losses and rights/dependency review. |
| GKC-24 | Business value and deployment fit | Does the workflow improve a defined business outcome against the current process, within the selected feature's availability and support conditions? | Held-out tasks, baseline, coverage, correctness, abstentions, review effort and deployment/version/support details. |

### How to record findings
Use the [shared assessment rules](../../guides/ai-context-evaluation.md#shared-dimension-framework-and-assessment-rules) for acceptance criteria, evidence status, outcomes and component responsibility. GKC-01 through GKC-24 map to the same numbered dimensions used by the other AI-context profiles.

## Industry example and boundaries
Proposed government case: discover an approved service-performance dataset and interpret its eligibility and reporting-period definitions. Evaluate discovery, semantic interpretation and lawful source access separately. This is an illustrative scenario, not an implemented case.

The docs' content footer specifies CC BY 4.0 and Apache 2.0 for code samples, subject to exceptions. That notice does not license the hosted service or determine rights in customer metadata. [S1] Runtime rights, region-specific availability, cache invalidation and complete context portability were not established.

## Official sources and evidence status
- [S1: About data context](https://docs.cloud.google.com/knowledge-catalog/docs/about-context), updated 13 October 2026.
- [S2: Retrieve context for data assets](https://docs.cloud.google.com/knowledge-catalog/docs/retrieve-data-context), updated 15 October 2026.

Checked 20 October 2026. No SIEL measurement of cross-agent consistency, answer quality or customer outcome is established.
