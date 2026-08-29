# Business Plan Creation

## Purpose

Create a decision-useful business plan that makes the opportunity, evidence, assumptions, and next validation priorities clear.

## Rules

Load:

- `.agents/rules/business/business-model-canvas.md`
- `.agents/rules/business/value-proposition.md`
- `.agents/rules/business/market-analysis.md`
- `.agents/rules/core/documentation-criteria.md`

## Inputs

Use the user's idea, supplied documents, and relevant existing project records. Review past decisions when their product, market, customer, or validation context can affect the current plan.

Before asking questions, extract what is already known. Ask for a user decision when competing answers would materially change the problem, target customer, value proposition, business model, or validation scope. Record other gaps as assumptions or unknowns.

## Process

1. Define the problem, affected customer, and evidence that the problem matters.
2. Describe the proposed value and the smallest hypothesis that needs validation.
3. Research current market and competitor claims. Cite sources and separate external evidence from inference.
4. Apply the relevant Business Model Canvas and Value Proposition Canvas elements to expose the model's important dependencies and trade-offs.
5. Identify validation priorities, success signals, material risks, and the next decision.
6. Write or update `projects/[project-name]/01-planning/business-plan.md`.

Create `market-research.md` when the research is substantial enough to be reused independently. Otherwise, keep the evidence and citations in the business plan.

## Business Plan Content

Include the sections needed to make the current business decision:

1. **Summary** — concept, target customer, value, and current decision
2. **Problem and Evidence** — customer problem, context, supporting evidence
3. **Proposed Value** — solution hypothesis, benefits, and differentiation
4. **Market and Alternatives** — market scope, competitors or substitutes, uncertainty
5. **Business Model** — relevant customers, channels, relationships, revenue, activities, resources, partners, and costs
6. **Validation Plan** — critical assumptions, MVP or experiment, success and failure signals
7. **Risks and Unknowns** — material risks, assumptions, missing evidence
8. **Next Decision** — what the evidence should enable the user to decide

Add financial projections, operations, organization, roadmap, or detailed go-to-market sections when the user requests them or they change the current decision. Label projections with their assumptions and source basis.

## Completion Criteria

- The problem, target customer, proposed value, and business model are understandable.
- Current external claims are cited with an access date.
- Facts, inferences, assumptions, and unknowns are distinguishable.
- Validation priorities can lead to an observable decision.
- Additional sections and supporting files have a stated use in the current plan or handoff.
