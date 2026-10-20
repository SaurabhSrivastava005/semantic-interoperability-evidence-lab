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

## Acceptance questions and difficult cases
| Proposed test | Evidence to retain |
|---|---|
| A source-owned measure changes | Source measure revision, ontology context and executed calculation |
| A natural-language rule conflicts with a source calculation | Both definitions, chosen authority and observed result |
| Imported ontology uses multiple inheritance | Original file, import log, resulting hierarchy and changed query answers |
| A relationship exists in sources but not in selected graph scope | Graph selection, refresh time and answer completeness |
| A definition version is restored | Definition diff, binding state and regression results |

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
