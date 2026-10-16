# Industry Standards Landscapes

This directory separates industry-specific standards from the [master standards and initiatives landscape](../standards-landscape.md).

The practical goal of this section is to help contributors turn a broad industry landscape into a small, testable and reusable interoperability profile. These documents are not meant to be encyclopaedias; they should help implementers answer: what problem are we solving, which authoritative sources are in scope, what can we safely reuse, and how do we validate the result?

Each industry landscape records:

- operational scope and priority use cases;
- relevant standards, models and frameworks;
- what each source provides;
- licensing and implementation boundaries;
- how SIEL should use the source;
- gaps that require evidence; and
- recommended first profiles.

## Practical industry pack structure

Each industry folder should include a compact implementation pack so contributors can quickly understand and test the domain:

- `standards-landscape.md` — human-readable overview of the domain and standards
- `README.md` — quickstart for that industry and links to profiles
- `industry.yaml` — machine-readable metadata for the sector
- `profiles/` — use-case-specific profile definitions
- `fixtures/` — synthetic example inputs and expected outputs
- `json-schema/` or other validation artefacts — rules for checking profile structure
- `tests/` — local or CI validation scripts

This makes the repository easier to search, easier to review in pull requests and easier to turn into evidence-backed profiles.

## Industry landscapes

| Industry | Landscape |
|---|---|
| Higher education and learning | [Higher education](higher-education/standards-landscape.md) |
| Healthcare and life sciences | [Healthcare](healthcare/standards-landscape.md) |
| Banking and financial services | [Financial services](financial-services/standards-landscape.md) |
| Energy and utilities | [Energy and utilities](energy-utilities/standards-landscape.md) |
| Real estate and construction | [Real estate and construction](real-estate-construction/standards-landscape.md) |
| Manufacturing, automotive and supply chain | [Manufacturing and supply chain](manufacturing-supply-chain/standards-landscape.md) |
| Government and public services | [Government and public services](government-public-services/standards-landscape.md) |
| Retail and consumer | [Retail and consumer](retail-consumer/standards-landscape.md) |

## Required maintenance fields

Every future machine-readable initiative record should include its steward, official source, jurisdiction, version, licence, artifact type, conformance support, evidence maturity and last verification date.

An initiative must not be described as open source merely because its documentation is publicly accessible.

## Minimum metadata for every industry profile

When creating or updating a profile, include these fields in the corresponding `industry.yaml` or profile manifest:

- `id`
- `title`
- `scope`
- `steward`
- `jurisdiction`
- `version`
- `license`
- `status`
- `evidence_maturity`
- `last_verified`
- list of `profiles`
- any privacy, safety or governance constraints

## Profile authoring checklist

Before a profile is treated as usable evidence, it should have:

1. a clear problem statement and bounded scope;
2. authoritative sources with version and licence metadata;
3. one or more synthetic example payloads;
4. explicit validation rules or mappings;
5. acceptance criteria for a successful implementation;
6. provenance and human review requirements; and
7. a clear designation such as `draft`, `experimental`, `validated` or `production`.

A profile is most useful when a team can read the landscape, review the profile and run a small validation locally without needing a broader research effort.
