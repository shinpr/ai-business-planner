# Document Review

## Purpose

Evaluate an existing business-planning document against its intended decision, audience, source material, and downstream use.

## Rules

Load `.agents/rules/core/documentation-criteria.md` and the rules matching the document type:

- Business plan: `.agents/rules/business/business-model-canvas.md`, `.agents/rules/business/value-proposition.md`, `.agents/rules/business/market-analysis.md`
- Requirements: `.agents/rules/business/mvp-definition.md`
- Design: `.agents/rules/business/design-thinking.md`
- Prototype prompt: `.agents/rules/business/prompt-engineering.md`

## Inputs

Use the target document, the sources it claims to follow, and the documents consumed immediately before or after it. Ask for the target path when it cannot be identified from the request.

## Review Process

1. Identify the document's purpose, audience, decision, and expected next consumer.
2. Check whether its required claims and decisions are supported by supplied material, project files, or cited external evidence.
3. Research current external claims when their accuracy affects the review conclusion.
4. Identify contradictions, missing decision-critical information, unsupported claims, and content whose required work has no effect on the document's purpose.
5. Present findings before changing the document.

Classify each finding:

- **Critical**: the document would cause an incorrect decision, invalid handoff, or materially misleading claim
- **Important**: the intended consumer lacks information needed to use the document reliably
- **Optional**: a potentially useful improvement whose absence does not prevent the intended use

For each finding, provide the evidence, impact, and smallest sufficient correction. Treat suggestions from frameworks and reviewers as candidates; a finding may be declined when it adds scope, duplicates evidence, or has no observable effect on the document's use.

## Review Output

```markdown
# Review: [document]

## Overall Assessment
[Whether the document can serve its intended use]

## Findings
### [Critical or Important] [title]
- Evidence: [document location and source]
- Impact: [decision or consumer affected]
- Smallest correction: [change]

## Accepted As-Is
- [Potential concern that is already sufficient, with reason]

## Optional Improvements
- [Suggestion and the value it may add]

## Required Decision
- [User-owned choice, or none]
```

## Updating the Document

Apply changes after the user selects them. Preserve the document's intent and user-provided facts, add citations for new external claims, and use Git history as the default version record.

Summarize applied and declined findings after the update. A repeated reviewer preference requires new evidence to change the previous resolution.

## Completion Criteria

- Findings trace to evidence and a named decision or consumer effect.
- Critical and important classifications use the definitions above.
- Optional improvements remain optional.
- Document changes match the user's selected findings.
- The updated document is rechecked against its intended use.
