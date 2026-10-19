# Business Context and Ontology Capabilities for AI
These are related vendor capabilities, not interchangeable implementations of one standard. All profiles are source-based drafts; implementation outcomes remain not-evaluated.

| Offering | Documented focus | Main implementation question |
|---|---|---|
| [Genie Ontology](databricks-genie-ontology.md) | Curated and inferred context for Genie | Which definition is selected, and why? |
| [Palantir Ontology](palantir-ontology.md) | Objects, relationships and operational actions | How do governed meaning and authorised actions connect? |
| [Fabric IQ ontology](microsoft-fabric-iq-ontology.md) | Entities, data bindings and metric context | Which source and calculation remain authoritative? |
| [Snowflake Semantic Views / Cortex Analyst](snowflake-semantic-views-cortex.md) | Business semantics for analytical SQL generation | Does the generated query preserve intended meaning? |
| [Google Knowledge Catalog](google-knowledge-catalog-context.md) | Metadata and business-context retrieval | What context reaches the consuming application? |

## Read the labels carefully
Genie Ontology is Public Preview and Fabric IQ ontology is Preview in the inspected documentation. No blanket availability or maturity label is assigned to the other offerings. Check the actual feature, deployment, region and release before relying on it.

A product capability is not the organisation-specific ontology or graph created with it. A shared category does not establish equivalent action support, inference, openness, portability or standards conformance.

## What SIEL should collect
- Specific business problem, acceptance criteria and baseline.
- Curated definitions versus inferred context and their authorities.
- Source data/model versions, access boundaries and update behaviour.
- Answer correctness, abstentions, conflict handling and provenance.
- Authorised action behaviour where actions are in scope.
- Maintenance effort, upgrades, migration and exit options.
- Official limits separately from measured implementation failures.

See [the evaluation guide](../../docs/ai-context-evaluation.md), [semantic catalogue](../semantic-and-knowledge-models.md) and [vendor catalogue](../vendors/README.md).
