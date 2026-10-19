# Palantir Ontology
- Catalogue ID: palantir-ontology
- Category: ai-business-context
- Subtype: operational-ontology
- Ownership: vendor-led
- Steward: Palantir
- Scope: cross-industry capability; organisation-specific context
- Maturity: Not established for every component; no blanket GA claim
- Editorial status: draft; independent reviewer pending
- Prepared by: Codex from official vendor sources
- Source checked: 2026-10-19
- Next review: 2027-04-19
- Regulatory status: not-assessed
- Implementation outcome: not-evaluated
- Licence verification: not-verified for runtime and customer-authored assets
- Source interests: product vendor, not an independent evaluator
- SIEL summary licence: CC BY 4.0; external assets retain their terms

## What it does and what it depends on
Palantir describes its Ontology as an operational layer connecting integrated data assets to real-world objects. It combines objects, properties and links with actions, functions and security controls.

Its scope includes operational workflows, not only context retrieval or metric definition. A customer's configured Ontology remains distinct from a reusable industry ontology and from the Palantir product itself.

Dependencies include the Palantir platform, mapped sources and the configured actions and functions. AIP integration adds an AI consumption context; this record does not assume every Ontology workflow requires AIP.

Product release, component maturity, deployment entitlements, export rights and equivalence outside Palantir were not established. No open asset licence is inferred from public documentation.

## Questions to evaluate in an implementation
- Which source owns each object property, and how are conflicting updates handled?
- Which actions can an agent propose versus execute?
- What authorisation, approval and rollback evidence exists?
- Can definitions and workflow logic be migrated with their behaviour intact?
No operational safety or portability outcome was tested by SIEL.

## Official sources
- [Official Ontology overview](https://www.palantir.com/docs/foundry/ontology/overview), Object and link types, Action types and functions.
- [AIP architecture](https://www.palantir.com/docs/foundry/architecture-center/aip-architecture), platform relationship; rolling vendor documentation.
Checked 2026-10-19. Product documentation establishes described capability, not implementation success.

## Evidence gap
No customer deployment, benchmark, portability result or maintenance-cost study was independently assessed in this record. Missing evidence is not failure. Apply the [evidence policy](../../docs/evidence-policy.md).
