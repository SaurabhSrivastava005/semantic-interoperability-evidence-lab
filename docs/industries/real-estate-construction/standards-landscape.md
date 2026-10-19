# Real Estate, Buildings and Construction Standards Landscape

## Scope

This landscape covers design, construction, building assets, operational technology, property information, digital twins and lifecycle exchange.

## Standards and models

| Standard or framework | Primary purpose | Availability and boundary | Potential relevance to investigate |
|---|---|---|---|
| [Industry Foundation Classes](https://www.buildingsmart.org/standards/bsi-standards/industry-foundation-classes/) | BIM and built-environment information exchange | Open international standard with mature tooling | Profile only the entities required by each lifecycle use case |
| [Brick Schema](https://brickschema.org/) | Building assets, systems, points and relationships | Open ontology and tooling | Evaluate for building operations and analytics |
| [RealEstateCore](https://www.realestatecore.io/) | Real-estate and building semantics | Open ontology, examples and tooling | Map property and operational concepts |
| [Project Haystack](https://project-haystack.org/) | Building and IoT semantic tagging | Open community specification and tools | Test telemetry and equipment tagging portability |
| [Google Digital Buildings](https://google.github.io/digitalbuildings/) | Installed-equipment and building ontology | Apache-licensed ontology and tools | Evaluate mappings with Brick and Haystack |
| [Asset Administration Shell](https://industrialdigitaltwin.org/en/content-hub/aasspecifications) | Digital representation of assets | Public specifications and implementations | Evaluate cross-industry asset lifecycle exchange |
| [W3C BOT](https://w3c-lbd-cg.github.io/bot/) | Building topology ontology | Public community specification | Use for spatial and topology mappings where suitable |
| [OGC standards](https://www.ogc.org/standards/) | Geospatial information and services | Public specifications with varied implementation maturity | Use for location and spatial-service profiles |

## Candidate use cases for evidence collection

1. Asset handover from construction to operations.
2. Equipment identity across BIM, BMS and maintenance systems.
3. Building energy and sustainability evidence.
4. Property and spatial identity reconciliation.
5. Digital-twin telemetry context.

Case records should state its lifecycle stage, geometry expectations, coordinate reference system, asset identity policy and acceptable semantic loss.

## Evidence status
This landscape lists discovery leads and candidate use cases. It does not establish successful adoption, conformance or failure. Add sourced [implementation cases](../../../implementations/README.md) and [exceptions](../../../exceptions/README.md) using the [evidence policy](../../evidence-policy.md).

## Sourced record drafts
[Building exchange guide](../../../use-cases/building-model-exchange.md), [GeoBIM case](../../../implementations/construction-geobim-ifc.md), [software interpretation exception](../../../exceptions/ifc-tool-interpretation.md) and [IFC source check](../../../registry/ifc.md).
Independent editorial review is pending. Historical case outcomes do not establish current product performance.

## Semantic and knowledge model discovery
[Brick](../../../registry/ontologies/brick.md) and [RealEstateCore](../../../registry/ontologies/realestatecore.md) describe building concepts. [DTDL](../../../registry/technologies/dtdl.md) is a modelling language, not the building ontology itself.
See the [semantic catalogue](../../../registry/semantic-and-knowledge-models.md). These are drafts; use-case outcomes have not been established.
