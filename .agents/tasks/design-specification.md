# Design Specification

## Purpose

Define the visual and interaction decisions that materially affect the prototype's intended experience or validation goal.

## Rules

Load:

- `.agents/rules/business/design-thinking.md`
- `.agents/rules/core/documentation-criteria.md`

## Inputs

Use the requirements, business context, supplied brand materials, and design references. Extract existing direction before asking questions.

Ask for a user decision when different choices would materially change brand identity, the primary interaction, accessibility, or the experience being validated. Use an evidence-supported default for reversible visual details and label material inferences.

## Process

1. Identify the primary user, context of use, core journey, and experience goal.
2. Translate relevant brand or atmosphere attributes into concrete interface direction.
3. Specify the screens, hierarchy, interactions, states, and responsive behavior required by the core journey.
4. Record accessibility requirements that apply to the selected users and platform.
5. Define reusable visual tokens or components only where consistency across the selected screens requires them.
6. Write or update `projects/[project-name]/03-design/design-requirements.md`.

Create separate UI concepts or assets when the user requests them or another selected task consumes them as files.

## Design Content

1. **Experience Goal** — intended feeling, usability outcome, and target context
2. **Design Direction** — atmosphere, visual hierarchy, color and typography direction, relevant references
3. **Core Screens and Flows** — required screens, transitions, and user feedback
4. **Interaction States** — applicable loading, empty, error, success, focus, and disabled states
5. **Responsive and Accessibility Requirements** — behavior and standards that affect the prototype
6. **Assumptions and Open Decisions** — inferred defaults and unresolved material choices

Use exact color values, type scales, breakpoints, component specifications, or brand assets when supplied or when the prototype needs them to reproduce an agreed direction.

## Completion Criteria

- Design decisions trace to the user, brand, requirements, or validation goal.
- The core journey has enough visual and interaction direction for prompt generation.
- Material responsive and accessibility behavior is specified.
- Reversible defaults are distinguishable from agreed requirements.
- Design detail remains proportional to the prototype scope.
