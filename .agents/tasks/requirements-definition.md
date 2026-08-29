# Requirements Definition

## Purpose

Define the smallest product scope that can deliver the agreed value and test the current business hypothesis.

## Rules

Load:

- `.agents/rules/business/mvp-definition.md`
- `.agents/rules/business/value-proposition.md`
- `.agents/rules/core/documentation-criteria.md`

## Inputs

Use the approved business plan when available. A direct requirements request can instead use supplied material that establishes the problem, target user, intended value, and validation goal.

Inspect the sources before asking questions. Ask when an unresolved choice would change the MVP outcome, included users, essential behavior, or success criteria. Label other gaps as assumptions or unknowns.

## Process

1. Extract the target user, problem, intended value, and hypothesis to validate.
2. Define the smallest complete user journey that can test that hypothesis.
3. Select essential behavior and explicit scope boundaries using MoSCoW or another prioritization already established by the project.
4. Describe user-visible behavior and acceptance criteria for the selected scope.
5. Record only the functional, quality, data, integration, accessibility, security, or platform constraints that affect the selected journey.
6. Define validation signals and failure conditions.
7. Write or update `projects/[project-name]/02-requirements/requirements.md`.

Create a separate `core-value.md` only when another consumer needs that statement independently from the requirements document.

## Requirements Content

1. **Outcome and Source** — intended value, validation goal, and links to governing material
2. **Users and Core Journey** — selected users and the minimum end-to-end journey
3. **MVP Scope** — essential behavior, priority rationale, and explicit exclusions
4. **Behavior and Acceptance Criteria** — observable results for the selected features
5. **Applicable Constraints** — only constraints that change implementation or validation
6. **Assumptions and Unknowns** — material uncertainty and its effect
7. **Validation** — success signals, failure signals, and evidence to collect

## Completion Criteria

- Every included behavior contributes to the stated outcome or its validation.
- The minimum user journey is complete enough to exercise the intended value.
- Acceptance criteria are observable.
- Scope boundaries, material assumptions, and unknowns are explicit.
- Requirements trace to their business or user source.
