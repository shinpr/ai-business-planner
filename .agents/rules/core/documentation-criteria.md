# Business Documentation Criteria

## Purpose

Choose the smallest durable document set that serves the user's current outcome and its known downstream consumers.

## Artifact Selection

Create or update a document when at least one condition applies:

- the user requested it;
- another selected task requires its decisions as input;
- it records a significant decision or evidence that would otherwise be lost;
- it is the agreed deliverable for review or handoff.

Reuse an existing document when it already owns the same information. Keep a result in the conversation when no downstream consumer or durable record needs a file.

## Document Types

| Document | Use when | Path |
|---|---|---|
| Session summary | Meeting notes need a reusable summary, actions, or extracted decisions | `05-sessions/` |
| Business plan | The current outcome requires business viability, market, value, or model decisions | `01-planning/business-plan.md` |
| Market research | External evidence is substantial enough to reuse separately from the plan | `01-planning/market-research.md` |
| Requirements | A product or prototype needs an agreed MVP scope and observable behavior | `02-requirements/requirements.md` |
| Design requirements | Visual or interaction decisions materially affect the prototype | `03-design/design-requirements.md` |
| Prototype prompt | The user will build a prototype with an AI generation tool | `04-prompts/[platform]-prompt.md` or `04-prompts/prototype-prompt.md` |
| Usage guide | The user requested reusable human instructions separate from the executable prompt | `04-prompts/[platform]-guide.md` |
| Decision record | A significant Go/NoGo, strategic, scope, or investment decision needs future reference | `06-decisions/` |
| Proposal | A stakeholder audience needs a presentation or decision package | `07-artifacts/` |

The complete business-planning workflow may produce several of these documents because its downstream phases consume earlier decisions. A phase-specific request produces only its selected deliverable and missing prerequisites that the user chooses to add.

## Document Boundaries

- Business plans own business opportunity, evidence, model, and validation assumptions.
- Requirements own MVP scope, user-visible behavior, constraints, and success criteria.
- Design requirements own material visual, interaction, responsive, and accessibility decisions.
- Prototype prompts own instructions pasted into the generation tool.
- Decision records own the decision, alternatives actually considered, rationale, impact, and review condition.

Link dependent documents rather than copying their full contents. Include an extracted fact when the downstream document needs it to be usable on its own.

## Evidence and Status

For material claims, distinguish:

- user-provided facts;
- cited external evidence;
- inferences and assumptions;
- unresolved unknowns.

Record approval when a downstream phase depends on an agreed business outcome, MVP scope, or major design direction. Semantically equivalent evidence of approval is sufficient; a fixed heading or status field is not required.

## Versioning

Git history is the default version record. Create a dated copy in `versions/` when the user needs a separately accessible snapshot or when an established project folder already uses that convention for handoff.

## Quality Criteria

A document is complete when:

- its purpose and audience are clear;
- the decisions required by its next consumer are present;
- material evidence, assumptions, and unknowns are distinguishable;
- dependent documents are linked;
- optional sections and artifacts are included when they change a decision or handoff.
