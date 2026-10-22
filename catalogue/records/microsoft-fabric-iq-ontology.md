# Microsoft Fabric IQ ontology

[Catalogue metadata](../index.yaml) · [Evidence policy](../../guides/evidence-policy.md) · [Comparison](../../guides/ai-context-comparison.md)

## Business problem and architecture
Fabric IQ's preview ontology defines entities, properties, relationships and bindings to enterprise sources. Namespaces, inheritance and shared properties support reuse. Source Power BI DAX measures remain owned by the semantic model; ontology adds metric context. Natural-language rules provide context to consumers. The ontology itself is not a general-purpose query engine. Workspace/item permissions and bound-source controls are part of the documented governance model. [S1]

SIEL assessment: distinguish a business rule described to an agent from a rule enforced by executable application or source logic. Keep the authoritative calculation identifiable when several sources describe the same metric.

## Graph execution is a separate choice
The graph documentation distinguishes semantic structure from optional instance-data materialization. Relationship-centric queries can use a selected materialized graph; the ontology does not require that execution path. Eligible entities and relationships must satisfy graph-specific source and key requirements. [S2]

Ask whether a proposed task needs graph traversal at all. If it does, measure materialization freshness and ensure the selected scope contains the paths needed by the question.

## Lifecycle and standards interoperability
Named version-history snapshots capture ontology definitions. The documented experience supports manual checkpoints and restoration; read-only users can view versions but cannot modify or restore them. [S3]

Import accepts supported TTL, RDF/RDFS and OWL into an empty ontology item, converting definitions into native elements. Export writes TTL or RDF. The import summary distinguishes preserved, adjusted and unsupported content. Documented adjustments include retaining only the first parent in multiple inheritance and possible conversion of unsupported property types to strings. [S4]

SIEL assessment: file-format support does not establish full OWL semantics, reasoning equivalence or lossless round trips. Treat the import report as evidence to review, not a certificate of conformance.

## Assessment dimensions and evidence
These 24 dimensions apply the shared SIEL framework to this offering and its consuming applications. They are proposed evaluation questions, not verified capabilities, observed defects or exhaustive coverage. Record component responsibility and any justified exclusions using the [shared assessment rules](../../guides/ai-context-evaluation.md#shared-dimension-framework-and-assessment-rules).

### Business meaning

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| FAB-01 | Semantic fidelity | Do entity properties, metrics and natural-language rules retain the source business meaning? | Approved definitions, ontology context and reviewed consumer outputs. |
| FAB-02 | Applicability and exceptions | Are domain namespaces, hierarchies and policy/date exceptions applied to the correct question? | Scoped definitions, hierarchy cases and tasks with distinct correct interpretations. |
| FAB-03 | Authority and conflict resolution | When ontology context conflicts with a bound source measure or rule, which owner and definition is authoritative? | Source/ontology definitions, ownership and selected calculation rationale. |
| FAB-04 | Traceability and revision identity | Can an answer be traced to the ontology version, binding and source-owned measure revision used? | Version identifier, bindings, measure revision and consumer trace. |

### Discovery and context quality

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| FAB-05 | Asset coverage and discovery | Which required sources, entity types and consumers work in the actual tenant, and what is excluded? | Tenant/source support inventory, binding checks and missing-coverage cases. |
| FAB-06 | Relevance and context completeness | Does an agent receive all rules, metric qualifiers and bindings needed for the question? | Supplied context, intended scope, omitted elements and answer comparison. |
| FAB-07 | Relationships, identity and mappings | Do keys, entity mappings, relationships and inheritance represent the intended business structure? | Source mappings, key/cardinality checks and hierarchy/identity cases. |
| FAB-08 | Metadata quality and source-data quality | Are ontology-definition defects distinguished from binding errors and source-data defects? | Separate validation/data checks and reviewed failure attribution. |

### Governance and change

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| FAB-09 | Freshness and propagation | How quickly do source and definition changes reach consumers and any materialized graph? | Timed changes, source/context/graph timestamps and observed results. |
| FAB-10 | Lifecycle and change control | What survives version restoration or migration, and which bindings, consumers or graph states need separate recovery? | Definition/binding diffs, migration logs, consumer regressions and recovery results. |
| FAB-11 | Uncertainty and missing context | Does the consumer explain missing bindings, unresolved meanings or unavailable metrics rather than invent a calculation? | Missing/ambiguous cases and actual clarification or abstention. |
| FAB-12 | Accountability and stewardship effort | Who maintains entities, source measures, bindings and optional graph scope across teams? | Ownership map, handovers, unresolved changes and maintenance hours. |

### Security and trust boundaries

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| FAB-13 | End-to-end authorization | Do item/workspace access and bound-source controls remain effective through each consumer and graph path used? | Identity chain, permitted/denied cases, revocation and query decisions. |
| FAB-14 | Privacy and information exposure | Can ontology metadata or graph/context outputs expose restricted source information? | Sensitive-property cases, visible payloads and log/cache access review. |
| FAB-15 | Untrusted context and instruction handling | How are untrusted business-rule text, imported labels or source descriptions handled by the consuming agent? | Controlled hostile definitions, consumer instructions and executed tool/query trace. |
| FAB-16 | Location, retention and use constraints | Are ontology, source, graph and model processing/retention locations acceptable for the deployment? | Actual data-flow map, configured locations, retention and relevant terms. |

### Consumer behaviour and reproducibility

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| FAB-17 | Downstream semantic correctness | Does the consumer use the source-owned calculation and the appropriate query/graph path to answer correctly? | Approved metric/path, execution trace and checked result. |
| FAB-18 | Cross-consumer consistency | Do different consuming experiences preserve equivalent business meaning on matched questions? | Matched ontology/source state, consumer configurations and reviewed outputs. |
| FAB-19 | Auditability and repeatability | Can an answer be reconstructed after ontology, source measure or graph state changes? | Permitted revisions/snapshots, graph scope/freshness, settings and replay differences. |
| FAB-20 | Failure handling and reliability | How does the workflow respond to failed bindings, unavailable sources, stale graphs or incomplete migrations? | Injected failures, fallback disclosure and recovery/regression evidence. |

### Operations, portability and value

| ID | Dimension | Evaluation question | Evidence to request |
|---|---|---|---|
| FAB-21 | Performance and scale | Do source queries and optional graph materialization/traversal meet representative workload targets? | Graph/source scope, load, refresh time, component latency and errors. |
| FAB-22 | Cost and operational burden | What do ontology authoring, source queries, graph materialization and ongoing review cost? | Dated capacity/consumption records, setup/review hours and accepted-task counts. |
| FAB-23 | Portability and interoperability | Which meanings survive RDF/OWL import and RDF/Turtle export, including unsupported constructs and bindings? | Original/exported files, import report, element comparison, receiving-system tests and rights. |
| FAB-24 | Business value and deployment fit | Does the selected preview experience deliver a useful outcome within actual tenant/source support limits? | Tenant/version details, baseline, held-out cases, coverage and reviewed business results. |

## Industry example and boundaries
Proposed utilities case: connect asset definitions to approved outage metrics and investigate affected equipment. Evaluate calculations against source measures and dependency paths against known topology separately. This is an illustrative evaluation, not an implemented customer case.

The inspected prerequisites require Fabric-enabled capacity and tenant enablement for the ontology item. Source/consumer availability and permissions require tenant-specific checks. No migration, graph workload, standards-conformance test or customer outcome was run.

## Official sources and evidence status
- [S1: Ontology overview](https://learn.microsoft.com/en-us/fabric/iq/ontology/overview).
- [S2: Materialize an ontology graph](https://learn.microsoft.com/en-us/fabric/iq/ontology/how-to-use-ontology-graph).
- [S3: Version history](https://learn.microsoft.com/en-us/fabric/iq/ontology/how-to-use-version-history).
- [S4: Import and export](https://learn.microsoft.com/en-us/fabric/iq/ontology/how-to-import-export).

Checked 20 October 2026; preview documentation, not production validation. See the existing [migration boundary](../../evidence/exceptions/fabric-iq-ontology-migration.md) and separate [Power BI record](power-bi-semantic-models.md).

See the [import fidelity boundary](../../evidence/exceptions/fabric-ontology-import-fidelity.md).
