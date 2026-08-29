# Prompt Engineering for Prototype Generation

## Purpose

Translate agreed requirements and design decisions into instructions a prototype-generation tool can execute and the user can verify.

## Prompt Inputs

Include information when it changes the generated result or its verification:

- product outcome and target user;
- usage context and core journey;
- selected MVP behavior and scope boundaries;
- observable acceptance criteria;
- material design, responsive, and accessibility direction;
- data, integration, or technology choices required by the prototype;
- the selected platform's relevant capabilities and constraints.

Reference source documents when the tool can access them. Extract the required facts when the prompt must be usable on its own.

## Structure

Use the smallest section set that makes the instructions and dependencies visible. A typical executable prompt contains:

1. outcome and context;
2. scope and exclusions;
3. user flows and system responses;
4. functional behavior and important states;
5. design direction;
6. data and technical direction;
7. completion criteria.

Describe behavior through user actions, system responses, and observable results. Add data examples, component detail, or edge cases when they remove an ambiguity that would materially change the prototype.

## Platform Adaptation

Use current official platform information when a platform-specific capability, syntax, limit, or default affects the prompt. Treat changing prices, credit limits, model behavior, and product defaults as current external claims that require verification.

For component-oriented UI generators, describe the component hierarchy and interaction states when those decisions matter. For full application generators, describe persistence and integrations according to the required prototype fidelity. A platform's default framework or component library remains acceptable when the requirements leave that choice open.

Component-library palette and shape defaults remain active by default. When an agreed visual direction exists, state the replacement tokens explicitly.

## Design Translation

Translate agreed atmosphere or brand direction into the smallest concrete set the tool needs, such as color semantics, typography direction, spacing density, shape, imagery, and interaction tone. Provide exact tokens when supplied or needed for reproducibility.

Describe visual exclusions only when a specific default would contradict the agreed direction. Pair the exclusion with the required alternative.

## Prompt Boundary

Executable prompt content instructs the generation tool. Human setup, usage, troubleshooting, iteration, and deployment guidance belongs in a requested guide rather than in the executable prompt.

## Verification

Read the prompt as a fresh tool session and check:

- the outcome and scope are unambiguous;
- required behavior traces to the source requirements;
- interactions and important states are observable;
- design detail is sufficient for the agreed direction;
- technical fidelity matches the validation goal;
- completion criteria let the user judge the generated result.
