# Palantir Ontology

[Catalogue metadata](../index.yaml) · [Evidence policy](../../guides/evidence-policy.md)

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

## Related records
- [evidence collection](../../evidence/README.md)
