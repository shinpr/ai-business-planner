# Task Analysis

## Purpose

Select the smallest existing task or workflow that can produce the user's requested outcome.

Use this task when a request spans multiple business-planning activities or its route is unclear. Direct requests and slash commands load their named task directly.

## Inputs

- The user's requested outcome and supplied materials
- Relevant existing documents under `projects/`

## Analysis

### 1. Identify the outcome

Record the result the user is asking for, not every related artifact that could be created.

### 2. Separate scope

Classify relevant information as:

- **Current state**: existing documents, decisions, and known constraints
- **Required now**: work necessary for the requested outcome
- **Possible later**: useful options that are not required now
- **Excluded**: boundaries stated by the user

### 3. Select the route

Choose one primary task from the Request Routing table in `AGENTS.md`. Add another task only when its output is a real prerequisite of the requested outcome.

Use `.agents/workflows/business-planning-workflow.md` when the user requests the complete idea-to-prototype sequence. For a request targeting one phase, run that phase's task and inspect whether its required input already exists.

### 4. Check missing evidence

Inspect supplied materials and existing project files before asking questions. Ask for a user decision when the missing information would materially change the business outcome, scope, authority, or a major design decision. Label other material gaps as assumptions or unknowns in the deliverable.

### 5. Define completion

Completion is the selected task's usable deliverable and required evidence. Related possibilities remain optional unless the user selects them.

## Output

Return a short routing decision:

```markdown
Task: [selected task or workflow]
Outcome: [observable result]
Inputs: [existing sources to use]
Required decisions: [user decisions needed before execution, or none]
Deliverable: [file or response the user will receive]
```

Then execute the selected task when no missing user decision blocks it.

## Completion Criteria

- The selected route directly serves the requested outcome.
- Required inputs and user-owned decisions are identified.
- Optional downstream work has not been made part of the current task.
