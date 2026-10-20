# Business Context and Ontology Capabilities for AI

Start with the business task. These offerings share vocabulary but do not implement one interchangeable standard. The profiles below hold the detailed architecture, sources, limits and proposed acceptance tests. This page is a navigation and assessment aid, not a product ranking.

## Which job are you investigating?
| Offering | Documented centre of scope | Inspect first | Detailed record |
|---|---|---|---|
| Databricks Genie Ontology | Curated and inferred context for Genie | Definition selection and source authority | [Profile](../catalogue/records/databricks-genie-ontology.md) |
| Palantir Ontology | Business objects connected to operational actions | Identity, action authorization and resulting state | [Profile](../catalogue/records/palantir-ontology.md) |
| Fabric IQ ontology | Business entities and source bindings | Calculation ownership and source/consumer alignment | [Profile](../catalogue/records/microsoft-fabric-iq-ontology.md) |
| Snowflake Semantic Views / Cortex Analyst | Governed analytical definitions and SQL generation | Grain, query semantics and result correctness | [Profile](../catalogue/records/snowflake-semantic-views-cortex.md) |
| Google Knowledge Catalog | Discovery and retrieval of asset context | Metadata delivered to the consuming application | [Profile](../catalogue/records/google-knowledge-catalog-context.md) |

Sources and checked dates are recorded once in each canonical profile. All five remain source-based drafts with implementation outcomes not-evaluated. Genie Ontology is Public Preview and Fabric IQ ontology is Preview in inspected documentation. Check other features individually; no blanket maturity label applies.

## Six dimensions for a useful comparison
The following is SIEL's analytical framework. It defines what evidence to seek, not verified feature parity.

| Dimension | What the reader needs to know | Misleading shortcut to avoid |
|---|---|---|
| Business meaning | Owner, definition, applicability, calculation and exceptions | One familiar term must have one meaning everywhere |
| Context delivery | Selected assets, retrieval identity, freshness and exact supplied context | A connector means every application consumes the same context |
| Computation | Execution engine, metric grain, joins, filters and result | A grounded prompt guarantees a correct calculation |
| Action | Allowed operation, execution identity, preconditions and final state | Read access authorizes a business write |
| Change | Definition/source revisions, invalidation, regression and recovery | A saved definition also restores external data and effects |
| Portability | Exported structure, preserved behaviour, dependencies and rights | JSON, RDF or an API alone proves interoperability |

## How to use the profiles
For analytical questions, begin with approved calculations and difficult joins. For discovery, retain the retrieval response before inspecting the agent answer. For operational work, evaluate proposed decisions and executed changes separately. For standards reuse, test the meaning preserved by conversion, including unsupported constructs.

Multiple capabilities may participate in one implementation. For example, catalogue context can help find an asset while a semantic model supplies its calculation and an application controls an action. Document the actual components and handoffs instead of attributing the final result to one product name.

Do not infer absence from an unanswered question in a profile. A documentation check is narrower than a complete feature audit. Unknown deployment, export or licensing conditions remain unknown until checked.

## Industry exceptions should be explicit
The same word can have legitimate scope differences. The [industry scenario worksheet](ai-context-evaluation.md#industry-scenario-worksheet) gives examples across all eight SIEL industries. These are proposed cases to investigate, not reports of customer adoption.

Use the [evaluation guide](ai-context-evaluation.md) to record evidence. Publish an [implementation case](../evidence/implementations/README.md) when there is a named deployment and a bounded outcome. Publish an [exception](../evidence/exceptions/README.md) for a sourced limitation with a clear scope. Keep exploratory concerns as questions.
