---
id: exception-cortex-analyst-prior-results
record_type: exception
editorial_status: draft
prepared_by: Saurabh/Codex from cited sources
independent_reviewer: pending
source_checked_on: '2026-10-19'
next_review: '2027-04-19'
catalogue_ids:
- snowflake-semantic-views-cortex
finding_type: vendor-capability-limit
provenance_notes:
  Cause category: documented conversational capability boundary
  Evidence type: vendor documentation, not a customer incident
---
# Cortex Analyst: follow-up references to previous SQL results

## Documented limit
The inspected Cortex Analyst documentation states that it does not have access to results of previous SQL queries. A follow-up referring to a prior result's position cannot rely on that result being available to Analyst.

## Implication and response
Test follow-up resolution in the complete application. Any application-side method of supplying context needs its own validation; SIEL has not tested a workaround. The statement is dated documentation, not a claim about every Snowflake agent or future release.

Source: [Cortex Analyst](https://docs.snowflake.com/en/user-guide/snowflake-cortex/cortex-analyst), Known limitations in multi-turn conversations.

[Related offering](../../catalogue/records/snowflake-semantic-views-cortex.md). Frequency, business impact and customer incidents were not assessed.
