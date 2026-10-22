# Palantir Ontology

[Catalogue metadata](../index.yaml) · [Evidence policy](../../guides/evidence-policy.md) · [Comparison](../../guides/ai-context-comparison.md)

## Business problem and architecture
Palantir positions the Ontology as an operational layer over integrated datasets, virtual tables and models. Objects, properties and links represent business entities; actions and functions represent changes and business logic. Interfaces support shared shapes across object types. [S1]

This scope makes the distinction between answering a question and changing a business state especially important. An organisation's configured ontology is also distinct from a reusable industry vocabulary. AI integration adds another consumer and execution path; do not assume every Ontology workflow requires AIP.

## Governance and execution boundary
The action-permissions documentation separates viewing, editing and applying action types. Applying an action depends on the affected objects, datasources and submission criteria. Crucially, documented row and column read controls do not themselves extend to the action's write; the page directs authors to pair them with marking or Classification-based Access Control for downstream protection. Read/write authorizations and action-log permissions have separate roles. [S2]

SIEL assessment: a successful retrieval permission test is insufficient evidence that a write or downstream side effect is authorised correctly. Inspect the actual configuration and identity at each step.

## Modelling and lifecycle work
Palantir's design guidance warns about modelling source-system or department silos, exposing unnecessary technical properties, combining distinct entities in one object and choosing one mechanism for every kind of logic. These are vendor-described design anti-patterns, not measured failure rates. [S3]

Proposed implementation work: agree entity identity and property ownership before joining sources; record how source updates interact with user edits; inventory action dependencies and externally visible effects. Require a reviewable change process, recovery procedure and regression set. Export fidelity, version-dependent behaviour and deployment rights need separate investigation.

## Assessment dimensions and evidence
These 24 dimensions apply the shared SIEL framework to this offering and its consuming applications. They are proposed evaluation questions, not verified capabilities, observed defects or exhaustive coverage. Record component responsibility and any justified exclusions using the [shared assessment rules](../../guides/ai-context-evaluation.md#shared-dimension-framework-and-assessment-rules).

### Business meaning

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| PAL-01 | Semantic fidelity | Do object properties, units and function/action meanings match the approved business definitions? | Domain model, property definitions and reviewed workflow outcomes. |
| PAL-02 | Applicability and exceptions | Are department, jurisdiction and effective-date exceptions represented without conflating distinct entities or policies? | Scoped models, exception rules and contrasting business cases. |
| PAL-03 | Authority and conflict resolution | Which source or owner prevails when integrated data, user edits and business rules disagree? | Property ownership, conflicting updates and resolved-state rationale. |
| PAL-04 | Traceability and revision identity | Can a decision be traced to the object state, backing source and function/action revision used? | Object/source revisions, function/action identifiers and decision trace. |

### Discovery and context quality

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| PAL-05 | Asset coverage and discovery | Are all required objects, actions and backing sources available to the workflow, and are exclusions visible? | Use-case inventory, available object/action sets and missing-coverage cases. |
| PAL-06 | Relevance and context completeness | Does the AI application select the necessary object properties, tools and constraints without unrelated context? | Supplied context/tool schemas, omitted constraints and decision differences. |
| PAL-07 | Relationships, identity and mappings | Are object identity, link cardinality and cross-system mappings valid, including duplicate and historical records? | Identity rules, link mappings and duplicate/history test cases. |
| PAL-08 | Metadata quality and source-data quality | Can schema/model defects be distinguished from faulty backing data or incorrectly applied edits? | Validation checks, source records and classified incidents. |

### Governance and change

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| PAL-09 | Freshness and propagation | How quickly do source changes and user edits become visible to decision-making applications? | Timed updates, observed object states and query/action timestamps. |
| PAL-10 | Lifecycle and change control | How are schema, function and action changes reviewed, deployed and recovered without breaking consumers? | Dependency inventory, change review, regression evidence and recovery demonstration. |
| PAL-11 | Uncertainty and missing context | Does the workflow expose incomplete state, ambiguous identity and conflicting evidence before a decision or action? | Ambiguous cases, displayed uncertainty and escalation/approval behaviour. |
| PAL-12 | Accountability and stewardship effort | Who owns object definitions, integrations, action policy and failed-operation resolution? | Named roles, handover/escalation records, review queues and effort. |

### Security and trust boundaries

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| PAL-13 | End-to-end authorization | Do view permissions, submission criteria, execution identity and write protections enforce intended authorization together? | Allowed/denied actions, identity chain, configured criteria and resulting protections. |
| PAL-14 | Privacy and information exposure | Can object properties, action outputs, notifications or logs disclose restricted information? | Restricted-data scenarios and review of each output/log destination. |
| PAL-15 | Untrusted context and instruction handling | Can malicious object text or retrieved documents steer an agent into an unauthorised operation? | Adversarial context, exposed tool set, approval decisions and actual action trace. |
| PAL-16 | Location, retention and use constraints | Do deployment, model calls and external action effects comply with location, retention and use requirements? | Data-flow map, deployment/terms, endpoints and retained operational records. |

### Consumer behaviour and reproducibility

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| PAL-17 | Downstream semantic correctness | Does a proposed action satisfy business preconditions and produce the intended final state, including side effects? | Approved preconditions, proposal, submitted parameters and component-by-component results. |
| PAL-18 | Cross-consumer consistency | Do different applications or agents interpret the same object state and action constraints consistently? | Matched state/tasks, application settings and reviewed decision differences. |
| PAL-19 | Auditability and repeatability | Can investigators reconstruct who proposed, approved and executed an operation against which state? | Linked decision/action records, identities, revisions and final-state evidence. |
| PAL-20 | Failure handling and reliability | How are stale-state actions, duplicate requests, partial side-effect failures and recovery handled? | Controlled failure/concurrency cases, resulting states and recovery/compensation evidence. |

### Operations, portability and value

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| PAL-21 | Performance and scale | Do object queries, function calls and actions meet workload targets at realistic volumes and concurrency? | Representative object/link counts, component latency, throughput and failures. |
| PAL-22 | Cost and operational burden | What do data preparation, modelling, indexing/querying, actions and ongoing review cost for the bounded workflow? | Dated consumption, deployment terms, setup/maintenance effort and accepted-task counts. |
| PAL-23 | Portability and interoperability | Which object definitions, links, functions and action behaviour can be recreated outside the platform? | Permitted exports/SDK artefacts, external recreation, semantic gaps and rights review. |
| PAL-24 | Business value and deployment fit | Does the deployed workflow improve a measured operational outcome within the selected components' support conditions? | Baseline, held-out workflows, state correctness, review effort and component/deployment versions. |

## Industry example and boundaries
Proposed manufacturing case: investigate an equipment alert and approve a maintenance intervention. Keep diagnosis quality, authorised work-order creation and the external maintenance system's final state as separate outcomes. This is a scenario, not deployment evidence.

Dependencies include mapped platform data, configured objects, actions/functions and the consuming application or AI integration. Public documentation does not establish entitlement, open licensing or behaviour-preserving portability.

## Official sources and evidence status
- [S1: Ontology overview](https://www.palantir.com/docs/foundry/ontology/overview).
- [S2: Action permissions](https://www.palantir.com/docs/foundry/action-types/permissions).
- [S3: Ontology design anti-patterns](https://www.palantir.com/docs/foundry/ontology/ontology-anti-patterns).
- [AIP architecture](https://www.palantir.com/docs/foundry/architecture-center/aip-architecture), retained architecture reference; not newly rechecked in this pass.

S1–S3 checked 20 October 2026. All are vendor documentation; implementation outcomes remain not-evaluated.

See the [read/write boundary record](../../evidence/exceptions/palantir-action-write-controls.md).
