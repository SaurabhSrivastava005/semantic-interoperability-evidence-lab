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

## Acceptance questions and difficult cases
| Proposed test | Evidence to retain |
|---|---|
| An agent suggests a valid action that its user cannot execute | Tool permissions, submitting identity, submission decision and audit record |
| Source data changes after a recommendation | Read revision, action parameters and stale-state handling |
| An action edits data and triggers an external effect | Outcome of each component, failure handling and duplicate-request behaviour |
| A property contains restricted information | Read policy, write authorization and protection on resulting data |
| Two systems identify the same real-world asset differently | Identity rules, link creation and resolution of conflicting properties |

These are evaluation questions; no transaction, rollback or security outcome was tested.

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
