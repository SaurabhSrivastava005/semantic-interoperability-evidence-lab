# Semantic and Knowledge Model Catalogue
All linked profiles are discovery drafts pending independent review. They do not establish implementation success.

| Category | Entries | What is being assessed |
|---|---|---|
| Domain ontologies and vocabularies | [FIBO](ontologies/fibo.md), [Brick](ontologies/brick.md), [RealEstateCore](ontologies/realestatecore.md), [SAREF](ontologies/saref.md), [Schema.org](ontologies/schema-org.md) | Definitions, relationships, constraints and domain coverage |
| Industry information models | [IEC CIM](ontologies/iec-cim.md) | Versioned industry objects and exchange context |
| Analytical semantic modelling | [Power BI](analytics/power-bi-semantic-models.md), [dbt/MetricFlow](analytics/dbt-semantic-layer.md), [Cube](analytics/cube-semantic-models.md), [LookML](vendors/google-looker-lookml.md) | Systems for authoring metrics and relationships; each authored model needs a separate case |
| Published knowledge graphs | [Wikidata](knowledge-graphs/wikidata.md), [DBpedia](knowledge-graphs/dbpedia.md) | Data assertions, provenance, release or revision and coverage |
| Languages and platforms | [DTDL](technologies/dtdl.md), [technology reference guide](technologies/README.md), [Neo4j](technologies/neo4j-platform.md) | Modelling or execution capabilities, not business models |

## Questions for end users
1. Is this a definition/schema, populated graph, modelling language or runtime?
2. Which version, jurisdiction and business question does it cover?
3. What concepts, local meanings or metrics need extension?
4. Which mappings, reasoners, databases, connectors or product entitlements are needed?
5. What implementation evidence supports the intended use?
6. How are revisions, disputes, missing data and maintenance handled?

## Evidence gaps
No new implementation success cases were established in this catalogue batch. The [DBpedia licensing boundary](../exceptions/dbpedia-dataset-licensing.md) is a publisher-documented condition, not a failure case.

Enterprise-specific graphs should be added through a [bounded implementation record](../templates/implementation.md) with publication authority. Product names, example models and announced partnerships are not substitutes.

See [classification](../docs/catalogue-classification.md), [evidence rules](../docs/evidence-policy.md) and [the verification log](../docs/source-verification.md).
