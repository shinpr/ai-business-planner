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

## Writing Principles

Write the desired prototype state, user behavior, system response, and observable result as positive, executable instructions. Express quality expectations as conditions the generated prototype can demonstrate rather than as advice to the generation model.

For each instruction or constraint, identify the source requirement, material ambiguity, platform behavior, or completion criterion it protects. Use the least-restrictive wording that preserves that need. Leave reversible presentation and implementation choices open when multiple choices satisfy the agreed outcome and verification criteria.

State necessary context once and near the instruction it controls. Include a section, example, edge case, technology choice, or procedure when it changes the generated result, protects a required boundary, resolves a material ambiguity, or enables verification. Leave other choices to applicable platform defaults.

Describe boundaries through the allowed scope and required alternative. Retain an explicit prohibition only when the prohibited action would be irreversible, the user could not normally recover from it, and positive wording alone would blur the boundary. Name the safe alternative and the condition that authorizes crossing the boundary.

Translate subjective quality labels and model-directed coaching into concrete artifact requirements. Keep a sentence when it changes a decision, action, generated result, or verification; otherwise omit it. When source material leaves an outcome-changing decision unresolved, state the missing decision instead of turning an inference into a constraint.

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
- instructions lead with the desired artifact or behavior;
- every constraint protects an identifiable source requirement, boundary, platform behavior, or completion criterion while leaving unrelated valid choices open;
- subjective quality language and model-directed coaching have been translated into observable artifact requirements;
- completion criteria let the user judge the generated result.
