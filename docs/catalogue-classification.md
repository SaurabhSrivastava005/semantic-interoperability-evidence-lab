# Catalogue Classification
A model's ownership does not determine its effectiveness or regulatory standing. Keep these dimensions separate.

| Field | Meaning | Values or recording rule |
|---|---|---|
| ownership_type | Who governs the asset | vendor-led, community-led, consortium-led, public-authority, mixed, not-assessed |
| model_category | What the asset is | common-data-model, industry-application-model, industry-model-family, business-domain-model, semantic-modelling-language, terminology, exchange-standard, reference-framework, domain-ontology, cross-domain-vocabulary, industry-information-model, analytical-semantic-modelling, published-knowledge-graph, graph-platform, technology-family, validation-language, other |
| regulatory_status | Applicable mandate | mandated, referenced, voluntary, not-assessed; include jurisdiction, version and authoritative source for any asserted status |
| access_class | What users can inspect | public, registration-required, entitlement-required, mixed, not-assessed |
| license_status | What rights were checked | source-stated, partial, not-verified; link exact asset terms |
| product_dependencies | Required or associated products | Identify what is required, merely associated or still unknown |
| implementation_outcome | Result of a bounded assessment | Apply evidence-policy labels; not-evaluated when no case has been assessed |
| verification_status | Source-check scope | Do not confuse source checking with editorial approval |

## Application
New vendor entries populate these fields in the YAML catalogue and explain uncertainties in their profiles. Older entries have not yet been backfilled; a missing field means not assessed, never public, voluntary or independent by default.

A vendor-led model may carry an open licence. A public reference model may impose reuse restrictions. A model addressing regulatory reporting is not automatically mandated. A semantic modelling language is not equivalent to a prebuilt sector model.

## Evidence
Documentation establishes documented scope. A release note establishes a vendor's notice. Neither is a customer implementation case. Require separate sources for outcomes, implementation effort and exceptions; preserve source interests and version boundaries.

## Semantic and graph asset boundaries
- Ontology or vocabulary: definitions, relationships and constraints.
- Industry information model: domain objects and contextual requirements.
- Analytical semantic modelling: a capability for authoring models; it is not one shared prebuilt industry model.
- Published knowledge graph: data assertions populated using one or more schemas.
- Modelling or query language: constructs for expressing or accessing models.
- Graph platform: storage and execution technology.

Use an implementation record to identify a specific organisation's model or populated graph. Record ontology/model version separately from dataset snapshot, instance revisions and runtime release. See [the semantic catalogue](../registry/semantic-and-knowledge-models.md).
