# Decision Recording

## Purpose

Create a reusable record of a significant Go/NoGo, strategic, product, scope, investment, or partnership decision.

## Rules

Load:

- `.agents/rules/business/decision-framework.md`
- `.agents/rules/core/documentation-criteria.md`

## Inputs

Use the decision statement, session record, business plan, requirements, and evidence relevant to the decision. A formal record begins after a decision has been made or when the user explicitly wants a proposal recorded as pending.

Ask for information when the decision itself, authority, or selected option is unclear. Preserve missing rationale, impact, ownership, or review conditions as unknown rather than inventing them.

## Process

1. State the decision, status, date, and decision maker when known.
2. Summarize the context and the evidence that made the decision necessary.
3. Record alternatives that were actually considered and their material trade-offs.
4. Explain the stated rationale, accepted trade-offs, and assumptions.
5. Record material impact, risks, success signals, follow-up actions, and a review condition when applicable.
6. Write `projects/[project-name]/06-decisions/YYYYMMDD-[decision-name].md`.
7. Update an existing decisions log when that project already maintains one.

## Decision Content

```markdown
# Decision: [name]

## Status
- Date: [date]
- Decision maker: [person or role]
- Status: [proposed, approved, rejected, or deferred]

## Decision
[What was decided]

## Context and Evidence
[Why the decision was needed and the evidence used]

## Alternatives Considered
- [Alternative and material trade-offs]

## Rationale and Assumptions
[Why the selected option was chosen]

## Impact and Risks
- [Material impact, risk, or accepted trade-off]

## Success and Review
- Success signal: [observable result]
- Review condition: [date, event, or evidence when applicable]

## Follow-up
- [Agreed action — owner — due date when known]
```

## Completion Criteria

- The decision and its status are unambiguous.
- Recorded alternatives reflect the actual decision process.
- Evidence, rationale, assumptions, impacts, and material risks are distinguishable.
- Follow-up work reflects agreed actions rather than technically possible additions.
- A future reader can tell when the decision succeeded or should be reconsidered.
