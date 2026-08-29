# Session Processing

## Purpose

Turn meeting notes or a transcript into a reliable summary of what was discussed, decided, assigned, and left unresolved.

## Inputs

Use the supplied session material and any context the user provides. Preserve the distinction between statements made in the session and later interpretation.

## Process

1. Identify the meeting purpose, date, participants when known, and discussion themes.
2. Extract decisions that were actually made, including stated rationale and decision maker when available.
3. Extract action items with owners and deadlines only when the source assigns them.
4. Record relevant requirements, customer or market insights, constraints, risks, and open questions.
5. Write `projects/[project-name]/05-sessions/YYYYMMDD-[session-name].md` when the user needs a durable session record.
6. Update an existing session index when that project already maintains one.

Use `.agents/tasks/decision-recording.md` when the user requests a formal record of a significant decision or the session identifies a decision whose future reuse requires the additional rationale and impact analysis.

## Session Content

```markdown
# Session: [name]

## Context
- Date: [known date or unknown]
- Participants: [known participants or unknown]
- Purpose: [meeting purpose]

## Summary
[Concise account of the discussion and outcome]

## Decisions
- [Decision, rationale, and decision maker when present]

## Actions
- [Action — owner — due date, using unknown where the source is silent]

## Requirements and Insights
- [Observed requirement or insight]

## Risks and Open Questions
- [Observed risk or unresolved question]
```

Include a section when it carries information useful to the session record's reader.

## Completion Criteria

- The summary represents the source material; decisions, owners, and deadlines appear only when the source states them.
- Decisions, actions, observations, and inferences are distinguishable.
- Unknown ownership or timing remains explicit when relevant.
- Any formal decision-recording follow-up has a named reuse need.
