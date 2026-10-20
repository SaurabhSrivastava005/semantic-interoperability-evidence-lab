# Evaluating AI Business Context and Ontology Capabilities
This is a set of questions for evidence collection, not a claim that SIEL has built or run a benchmark.

## Define the unit of evaluation
Name the product feature, deployment version, business domain, curated model, inferred sources, users and intended task. Compare only capabilities relevant to that task. An operational-action workflow and a read-only analytical assistant need different acceptance criteria.

## Record evidence for each question
| Question | Evidence to request |
|---|---|
| Which definition applies? | Competing definitions, policy authority, selected context and rationale |
| Does the answer preserve business logic? | Expected answer, metric grain, filters, generated query and actual result |
| Is uncertainty handled? | Ambiguous or missing-context questions, abstention and escalation behaviour |
| Is the source traceable? | Definition version, source revision, citation and transformation record |
| Do permissions hold? | Authorised and unauthorised user scenarios across source, retrieval and action |
| What changes when a source changes? | Before/after context, invalidation delay and regression results |
| Are actions controlled? | Approval boundary, execution identity, audit evidence and rollback where relevant |
| What does maintenance cost? | Authoring, curation, review and upgrade effort with measurement period |
| Can the organisation leave? | Exported definitions, rights, mapping work and demonstrated behaviour outside the product |

## Compare against a baseline
Use a stated alternative, such as existing curated semantic definitions or the current manual process. Report accuracy together with attempted task coverage, abstentions, review effort, latency and cost. State sample size, task selection and conflicts of interest. Do not derive an industry success rate from a handful of cases.

## Publish bounded conclusions
Separate vendor-described features, proposed tests, reported implementation results and independently reproduced evidence. A documentation limit belongs in an exception record with version/date context. A speculative concern remains a question until evidence supports a finding.

Publicly inspectable documentation does not establish rights to the runtime, customer-authored ontology, inferred context, source data or exported model. Record these separately.

[Browse offerings](ai-context-comparison.md) · [Implementation template](../templates/implementation.md) · [Exception template](../templates/exception.md).

## Separate the stages before judging the outcome
For each attempted task, retain a record covering: user question and identity; approved business interpretation; source and definition revisions; retrieved context; generated query or proposed action; execution identity; result or state change; and reviewer judgement. Record errors and abstentions as well as completed tasks.

Use explicit outcomes:
- Discovery: did the application find the relevant authorised asset?
- Meaning: did it select the definition applicable to this industry, organisation and date?
- Calculation: did the query or function implement the approved logic?
- Action: was the operation authorised, and did the intended state change occur?
- Maintenance: did correctness persist after a realistic source or definition change?

A case may succeed at discovery and fail at calculation. Report that boundary rather than compressing the case into a single success label.

## Product-specific evidence packets
| Capability being assessed | Additional artefacts to request |
|---|---|
| Inferred agent context | Candidate and selected snippets, source approval state, conflict review and retirement/change demonstration |
| Operational ontology | Object identity mappings, action configuration, authorization path, side-effect outcomes and recovery evidence |
| Data-bound ontology | Binding definitions, authoritative measure revision, import report, version checkpoint and optional graph scope/freshness |
| Analytical semantic view | Semantic definition, question/expected SQL pairs, actual result sets, evaluation configuration and per-question regressions |
| Catalogue context retrieval | Asset discovery result, lookup options, exact context response, caller identity and consuming application's query/tool call |

These packets correspond to the scopes described in the [canonical profiles](ai-context-comparison.md). They are requested evidence, not claims that every product exposes each artefact.

## Industry scenario worksheet
All rows are hypothetical research starting points. None represents a reported implementation or a claim of vendor support. Ask the domain owner to specify the actual rules and authoritative sources.

| Industry | Bounded business question | Exception to make explicit | Evidence of a useful result |
|---|---|---|---|
| Higher Education & VET | How many funded learners were enrolled on the census date? | Person, enrolment and participation differ; rules vary by funding scheme | Approved population, dates, exclusions and comparison with an authorised report |
| Healthcare & Life Sciences | Which encounters meet an approved study definition? | Local coding, missing observations and consent scope | Versioned cohort logic, mapping review and discrepancies assessed by domain reviewers |
| Banking & Financial Services | What exposure belongs to this counterparty group? | Legal entity, account and consolidated group differ | Identity/aggregation rules, effective dates and reconciliation to approved records |
| Energy & Utilities | Which assets are affected by a specified outage? | Network topology, connectivity state and reporting metrics have different owners | Known dependency paths, source timestamps and approved outage calculation |
| Real Estate & Construction | Which spaces and assets are in the delivered building model? | Tool interpretation, identifiers and project-phase changes | Source model/version, mapping decisions and comparison with accepted deliverables |
| Government & Public Services | Which applications meet the service-reporting definition? | Eligibility, jurisdiction, reporting period and policy version | Approved rule interpretation, authorised population and explained exclusions |
| Manufacturing & Supply Chain | Which orders are affected by a failed component? | Part revision, lot, supplier identity and approved substitute differ | Traceable dependency paths, revision scope and reviewed action boundaries |
| Retail & Consumer | What are net sales by region for the reporting period? | Returns, discounts, exchange rates and posting dates alter the answer | Approved formula, grain, dated conversion policy and reconciled results |

## Effort, cost and exit evidence
Record work by role: domain definition/review, source integration, semantic authoring, access configuration, application integration and ongoing change review. Separate initial setup from routine maintenance and incident correction. Use observed hours and a stated measurement period; do not invent typical implementation durations.

Record model/inference, query compute, indexing/materialization, metadata operations and human review separately where relevant. Do not compare headline prices for unlike tasks. Retain the pricing date and deployment conditions.

For an exit exercise, request the definitions and mappings the organisation is entitled to export. Recreate one bounded question outside the original consumer and report what survives: identifiers, terminology, calculations, permissions, action behaviour and provenance. Export availability, semantic fidelity and legal reuse are separate findings.

## What would support a publication?
A useful case names the organisation or explains anonymisation, identifies the deployed components and version/date, defines the task and baseline, reports attempted coverage and reviewed outcomes, and includes failures, exclusions and maintenance effort. Vendor self-reports must be labelled as such; a product example alone is not an implementation case.

This research pass adds documentation depth and proposed scenarios. It does not add independently reviewed successful or failed implementations.
