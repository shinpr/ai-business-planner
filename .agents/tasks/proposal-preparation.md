# Proposal Preparation

## Purpose

Create a Marp-compatible proposal or pitch deck that helps a specific audience make the requested decision.

## Inputs

Use the relevant business plan, requirements, research, prototype material, design direction, and the user's stated audience and ask.

Ask for the audience or requested decision when either is unknown. Infer the shortest coherent narrative from the available sources rather than copying every source section into slides.

## Process

1. Identify the audience, decision, ask, and evidence most likely to affect that decision.
2. Select a narrative that establishes the problem, proposed response, supporting evidence, trade-offs, and requested next step.
3. Create one primary message per slide, supported by the minimum text, data, or visual reference needed to communicate it.
4. Cite market data, projections, quotes, and other external claims.
5. Write `projects/[project-name]/07-artifacts/presentations/proposal-slides.md`.

Create speaker notes or additional appendix slides when requested or when they carry detail needed for the presentation but not the primary slide narrative.

## Marp Contract

The deck begins with valid Marp frontmatter and uses `---` as the slide separator.

```markdown
---
marp: true
paginate: true
---

# [Decision-oriented title]

[Message or evidence]
```

Choose slides from the decision's needs. Common candidates include:

- problem and evidence;
- target customer and value proposition;
- product or MVP demonstration;
- market and alternatives;
- business model;
- validation or traction;
- material risks and trade-offs;
- roadmap or financial implications;
- ask and next step.

Select a candidate when it changes the audience's understanding or decision. Combine candidates when one complete message can serve the same purpose.

## Completion Criteria

- The deck addresses a named audience and decision.
- Each slide communicates one primary message and fits within a readable slide boundary.
- Claims and projections trace to sources or labeled assumptions.
- The narrative leads to a clear ask or next step.
- Marp can parse the markdown structure.
