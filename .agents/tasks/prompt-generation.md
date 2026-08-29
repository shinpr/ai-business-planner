# Prompt Generation

## Purpose

Generate a prototype prompt containing the context and constraints needed to reproduce the agreed MVP, either for the user's selected tool or as a platform-independent handoff.

## Rules

Load:

- `.agents/rules/business/prompt-engineering.md`
- `.agents/rules/business/mvp-definition.md`
- `.agents/rules/core/documentation-criteria.md`

Load `.agents/rules/business/design-thinking.md` when design requirements exist.

## Inputs

Use the requirements, relevant business context, design requirements when present, and the user's selected generation platform when one has been selected.

Ask for the platform when its capabilities would materially change the prompt. Ask about fidelity or technical choices only when different answers would change the validation goal or executable output. Infer reversible presentation details from the source documents and label material assumptions.

## Scope Decision

Match implementation fidelity to the prototype's validation goal:

- Use mock data, local state, and simulated integrations when the outcome is a visual or interaction prototype.
- Include real persistence, authentication, APIs, or platform services when the validation goal requires their observable behavior and the selected tool can support them.
- Include production infrastructure only when it belongs to the agreed prototype scope.

## Prompt and Guide Boundary

The prompt file contains only content intended for execution by the generation tool. Platform introductions, account setup, copy-paste instructions, troubleshooting, and post-generation guidance belong in a separate guide when the user requests reusable usage documentation.

Decision test:

> Would the user paste this section into the generation tool to produce the prototype?

- Yes: include it in the executable prompt file.
- No: place it in `[platform]-guide.md` when the user requested reusable guidance.

## Process

1. Extract the outcome, users, core journey, essential behavior, scope boundaries, and acceptance criteria.
2. Integrate the design requirements when present. Otherwise, derive a minimal atmosphere direction from the relevant business context and industry characteristics.
3. Select technical and data instructions according to the prototype scope decision.
4. Apply current platform-specific guidance from `.agents/rules/business/prompt-engineering.md` when a platform is selected.
5. Write `projects/[project-name]/04-prompts/[platform]-prompt.md` for a selected platform, or `projects/[project-name]/04-prompts/prototype-prompt.md` for a platform-independent handoff.
6. Create `[platform]-guide.md` when requested.

Generate prompts for multiple platforms only when the user requests multiple outputs. A generic prompt is useful when the user has not selected a platform or explicitly needs a platform-independent handoff.

## Prompt Content

1. **Outcome and Context** — product purpose, users, scenario, and value
2. **Scope** — selected MVP behavior and exclusions
3. **User Flows** — actions, system responses, and important states
4. **Functional Requirements** — observable behavior and acceptance criteria
5. **Design Direction** — relevant visual, responsive, and accessibility requirements
6. **Data and Technical Direction** — only details that affect the prototype
7. **Completion Criteria** — observable behavior the generated result must demonstrate

## Completion Criteria

- The prompt is ready to paste into the selected tool or use as a platform-independent handoff.
- Every required instruction traces to the requirements, design, platform, or validation goal.
- The prompt and optional human guidance are separated by their consumer.
- Implementation fidelity matches the prototype's validation goal.
- Optional features, platforms, and production concerns appear in the prompt when the user selects them.
