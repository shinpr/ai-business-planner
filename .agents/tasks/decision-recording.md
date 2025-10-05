# Decision Recording

## Required Rules [MANDATORY - MUST BE ACTIVE]

**RULE AVAILABILITY VERIFICATION:**
1. [LOAD] `.agents/rules/business/decision-framework.md`
2. [LOAD] `.agents/rules/core/documentation-criteria.md`
3. [VERIFY ACTIVE] `.agents/rules/core/metacognition.md` (from session start)

## Purpose

Document significant business decisions, especially Go/NoGo decisions, with full context, rationale, and implications for future reference.

## Relationship with Session Processing

**Decision Flow**:
1. **Decision is made** in meeting/discussion
2. **Session Processing** (`.agents/tasks/session-processing.md`) extracts decision from meeting notes
3. **Decision Recording** (this task) creates formal decision document with full analysis

**When to Use**:
- After session-processing.md identifies a significant decision
- For formal Go/NoGo decisions
- For strategic business decisions requiring detailed documentation

**Key Difference**:
- **session-processing.md**: Extracts decisions from meeting notes (what was decided)
- **decision-recording.md**: Formal documentation with options analysis, rationale, and implications (why and how)

## Entry Conditions

□ Significant decision has been made (often identified by session-processing.md)
□ Decision context is understood
□ Decision impact identified
□ All required rules loaded and active

## Decision Types

### Go/NoGo Decisions
- Proceed with project/feature
- Investment decisions
- Launch decisions
- Pivot decisions

### Strategic Decisions
- Market positioning
- Business model changes
- Partnership decisions
- Resource allocation

### Product Decisions
- Feature prioritization
- Technical architecture
- Design direction
- Scope changes

## Decision Document Structure

### 1. Decision Summary
- Decision made (clear, concise)
- Date and decision makers
- Type of decision (Go/NoGo, Strategic, Product, etc.)
- Status (Proposed/Approved/Rejected/Deferred)

### 2. Context
- Background and situation
- Problem or opportunity
- Why this decision was needed
- Timing considerations

### 3. Options Considered
- Option 1: [Description, Pros, Cons]
- Option 2: [Description, Pros, Cons]
- Option N: [Description, Pros, Cons]

### 4. Decision Rationale
- Why this option was chosen
- Key factors in decision
- Trade-offs accepted
- Assumptions made

### 5. Impact and Implications
- Business impact
- Resource implications
- Timeline effects
- Risk implications

### 6. Success Criteria
- How to measure success of this decision
- Key metrics
- Validation approach

### 7. Next Steps
- Immediate actions required
- Responsibilities assigned
- Deadlines set
- Dependencies identified

### 8. Risks and Mitigation
- Risks associated with this decision
- Mitigation strategies
- Contingency plans

## Execution Process

### Step 1: Capture Decision
- Document what was decided
- Record who made the decision
- Note when decision was made

### Step 2: Provide Context
- Explain the situation
- Describe the problem/opportunity
- Document why decision was needed

### Step 3: Document Options
- List all options considered
- Analyze pros and cons
- Compare alternatives

### Step 4: Explain Rationale
- Why this option was selected
- Key decision factors
- Trade-offs and assumptions

### Step 5: Assess Impact
- Business implications
- Resource requirements
- Timeline effects
- Risk considerations

### Step 6: Define Success
- Set success criteria
- Identify metrics
- Plan validation

### Step 7: Plan Next Steps
- List immediate actions
- Assign responsibilities
- Set deadlines

## Deliverables

Primary:
- `projects/[project-name]/06-decisions/YYYYMMDD-[decision-type]-decision.md`

Supporting:
- `projects/[project-name]/06-decisions/decisions-log.md` (updated)

## Decision Document Template

```markdown
# Decision: [Decision Name]

## Metadata
- **Date**: YYYY-MM-DD
- **Decision Makers**: [Names/Roles]
- **Type**: [Go/NoGo/Strategic/Product/Other]
- **Status**: [Approved/Rejected/Deferred]

## Decision Summary
[Clear, concise statement of what was decided]

## Context
[Background, situation, why this decision was needed]

## Options Considered
### Option 1: [Name]
- **Description**: [Details]
- **Pros**: [Benefits]
- **Cons**: [Drawbacks]

### Option 2: [Name]
- **Description**: [Details]
- **Pros**: [Benefits]
- **Cons**: [Drawbacks]

## Decision Rationale
[Why this option was chosen, key factors, trade-offs, assumptions]

## Impact and Implications
- **Business**: [Impact on business]
- **Resources**: [Resource implications]
- **Timeline**: [Timeline effects]
- **Risks**: [Risk implications]

## Success Criteria
- [How to measure success]
- **Key Metrics**: [Metrics to track]
- **Validation**: [How to validate]

## Next Steps
1. [ ] [Action 1] - Owner: [Name] - Due: [Date]
2. [ ] [Action 2] - Owner: [Name] - Due: [Date]

## Risks and Mitigation
- **Risk**: [Description] - **Mitigation**: [Strategy]

## References
- Business Plan: [Link]
- Requirements: [Link]
- Related Decisions: [Links]
```

## Completion Conditions

□ Decision clearly stated
□ Context fully documented
□ Options analyzed
□ Rationale explained
□ Impact assessed
□ Success criteria defined
□ Next steps planned
□ Risks identified with mitigation
□ Document complete and accessible
□ Decisions log updated

## Common Pitfalls to Avoid

1. **Vague decision statement** → Be clear and specific
2. **Missing context** → Always explain why
3. **No options analysis** → Show alternatives considered
4. **Weak rationale** → Explain decision factors thoroughly
5. **Ignoring risks** → Identify and address risks
6. **No success criteria** → Define measurable outcomes
7. **Missing next steps** → Always plan follow-up actions

## Exit Conditions

□ Decision document exists and is complete
□ All completion conditions satisfied
□ Decisions log updated
□ Stakeholders informed
□ Ready to execute on decision
