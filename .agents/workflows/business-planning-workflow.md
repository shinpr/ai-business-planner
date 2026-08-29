# Business Planning Workflow

## Purpose

Use this workflow when the user requests an end-to-end path from a business idea or meeting notes through an approved prototype-generation prompt.

For a request targeting one deliverable, run the corresponding task directly.

## Workflow

### 1. Establish the business direction

Apply `.agents/tasks/business-plan-creation.md`.

Use supplied material, relevant past decisions, and current external evidence to produce the business plan. Present the resulting problem, target customer, value proposition, key assumptions, and validation priorities to the user.

Proceed to product requirements after the user agrees with the business direction. Incorporate requested corrections in this phase before downstream documents depend on it.

### 2. Define the MVP

Apply `.agents/tasks/requirements-definition.md` using the agreed business plan.

Produce the MVP scope, priority decisions, user-visible behavior, constraints, and validation criteria. Proceed after the user agrees with the MVP scope.

### 3. Decide whether design needs specification

Determine whether visual or interaction decisions materially affect the prototype:

- When the user has brand requirements, important interaction constraints, accessibility requirements, or a design-dependent validation goal, apply `.agents/tasks/design-specification.md` and obtain agreement on the major direction.
- Otherwise, continue directly to prompt generation, which derives a minimal atmosphere direction from the existing business context.

Ask the user when the available evidence leaves a choice between materially different intended experiences.

### 4. Generate the prototype prompt

Apply `.agents/tasks/prompt-generation.md` using the agreed requirements and any design requirements.

Generate the prompt for the platform selected by the user. Create a separate usage guide only when the user requests reusable instructions beyond the executable prompt.

## Independent Tasks

These tasks remain available before, during, or after the workflow when their outcome is requested:

- `.agents/tasks/session-processing.md`
- `.agents/tasks/decision-recording.md`
- `.agents/tasks/document-review.md`
- `.agents/tasks/proposal-preparation.md`

These independent tasks remain optional during the end-to-end workflow.

## Completion

The workflow is complete when:

- the business direction and MVP scope are agreed;
- material assumptions and unknowns are visible;
- design decisions are included when they affect the prototype;
- the selected platform prompt is ready to use;
- dependencies between produced documents are linked.

Summarize the outputs and offer proposal preparation, decision recording, or further validation as optional next actions when relevant.
