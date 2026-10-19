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
