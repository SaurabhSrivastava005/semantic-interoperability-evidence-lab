# Higher Education and Learning Standards Landscape

## Scope

This landscape covers institutional architecture, student administration, curriculum, learning platforms, credentials, mobility, research information and regulatory reporting.

No single source covers the complete university operating model. This guide helps users identify relevant standards and find evidence for bounded use cases.

## Standards and frameworks

| Standard or framework | Domain | What it provides | Potential relevance to investigate |
|---|---|---|---|
| [CAUDIT HERM](https://www.caudit.edu.au/communities/caudit-higher-education-reference-models) | Higher education enterprise architecture | Business, data, application and technology reference models | Optional external reference only. Do not copy, adapt or bundle restricted assets without written permission |
| [CEDS](https://ceds.ed.gov/) | Early learning, K-12, postsecondary, adult education and workforce | Common vocabulary, definitions, reference models and integration tools | Reuse as a cross-sector vocabulary source and test mappings |
| [Project Unicorn](https://www.projectunicorn.org/) | Primarily K-12 ecosystem adoption | Interoperability pledge, rubrics, certification resources and procurement guidance | Use for adoption and vendor-accountability practices, not as an API or data model |
| [Ed-Fi](https://docs.ed-fi.org/reference/data-exchange/data-standard/) | Primarily K-12 operational and analytical data | CEDS-aligned data standard, REST APIs and open technology suite | Evaluate at school-to-tertiary boundaries |
| [1EdTech Edu-API](https://www.1edtech.org/standards/edu-api) | Higher education administration | Models and APIs for exchanging core academic data | Candidate for enrolment, course and academic enterprise contracts |
| [PESC standards](https://pesc.org/approved-standards/) | Admissions and academic records | Transcript, admission, test-score and education-record formats | Profile relevant records and test cross-standard mappings |
| [1EdTech CASE](https://www.1edtech.org/standards/case) | Curriculum and competencies | REST exchange for competencies, standards and learning outcomes | Use for curriculum and outcome semantics |
| [1EdTech LTI](https://www.1edtech.org/standards/lti) | Learning tools | Secure LMS and tool integration | Use for delegated tool launch and context |
| [1EdTech OneRoster](https://www.1edtech.org/standards/oneroster) | Rostering and grades | CSV and REST exchange with certification | Evaluate at school and learning-platform boundaries |
| [Open Badges](https://www.1edtech.org/standards/open-badges) and [CLR](https://www.1edtech.org/standards/clr) | Achievements and learner records | Portable achievement, competency and experience records | Use for verifiable learner evidence |
| [European Learning Model](https://esco.ec.europa.eu/en/about-esco/escopedia/escopedia/european-learning-model) | Qualifications and credentials | Multilingual semantics for learning opportunities, qualifications and accreditation | Map qualifications and credential concepts |
| [EMREX](https://emrex.eu/) | Academic mobility | Learner-controlled academic-result exchange | Test transcript portability patterns |
| [FAIR Principles](https://www.go-fair.org/fair-principles/) | Research data | Findable, accessible, interoperable and reusable data and metadata principles | Apply to research and evidence assets, not as a schema or API |
| [CERIF](https://eurocris.org/services/main-features-cerif) and [VIVO](https://vivoweb.org/) | Research information | Research entities, relationships and knowledge graphs | Evaluate for institutional research profiles |
| [ORCID](https://orcid.org/) and [ROR](https://ror.org/) | Persistent identity | Researcher and organisation identifiers | Use for identity reconciliation |
| TCSI, AVETMISS, USI, CRICOS and TEQSA collections | Australian regulation and reporting | Authoritative definitions, validations and reporting obligations | Record jurisdiction-specific reporting requirements separately from operational models |
| [HL7 FHIR](https://hl7.org/fhir/) | University health and clinical research | Modular healthcare resources and APIs | Optional clinical overlay for academic medical centres and university health services |

## CAUDIT HERM boundary
The official page states CC BY-NC-SA 4.0 alongside additional usage wording. See the [source-checked profile](../../../registry/caudit-herm.md) for scope, access and unresolved interpretation. SIEL links to the steward and does not redistribute model files. Clarification is needed for reuse not clearly covered by the applicable terms.

## Candidate use cases for evidence collection

1. Credit transfer and recognition of prior learning.
2. Student application to enrolment exchange.
3. Curriculum, competency and learning-outcome alignment.
4. Portable learner achievement and transcript exchange.
5. Researcher, project and research-output discovery.

For each use case, collect relevant standards, published implementation outcomes, local exceptions and unresolved questions.

## Evidence status
This landscape lists discovery leads and candidate use cases. It does not establish successful adoption, conformance or failure. Add sourced [implementation cases](../../../implementations/README.md) and [exceptions](../../../exceptions/README.md) using the [evidence policy](../../evidence-policy.md).

## Sourced record drafts
[Learner-record guide](../../../use-cases/learner-record-exchange.md), [DUO case](../../../implementations/education-duo-emrex.md), [recognition boundary](../../../exceptions/emrex-recognition-boundary.md), [EMREX licence check](../../../registry/emrex-elmo.md) and [HERM source check](../../../registry/caudit-herm.md).
Independent editorial review is pending. Historical case outcomes do not establish current product performance.

## Vendor model discovery
Microsoft's CDM repository links a higher-education accelerator. See [the CDM profile](../../../registry/vendors/microsoft-cdm.md); current accelerator support and implementation results have not been verified.
These are draft catalogue leads, not implementation endorsements. Use the same evidence requirements as for community models.
