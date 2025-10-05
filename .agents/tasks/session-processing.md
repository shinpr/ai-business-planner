# Session Processing

## Required Rules [MANDATORY - MUST BE ACTIVE]

**RULE AVAILABILITY VERIFICATION:**
1. [LOAD] `.agents/rules/core/documentation-criteria.md`
2. [LOAD] `.agents/rules/business/decision-framework.md` (recommended)
3. [VERIFY ACTIVE] `.agents/rules/core/metacognition.md` (from session start)

## Purpose

Process meeting notes, discussion transcripts, or session recordings to extract key information, decisions, and action items.

## Entry Conditions

□ Session notes/议事录/meeting minutes provided by user
□ Session context understood
□ All required rules loaded and active

## Processing Outputs

### 1. Session Summary
- Date and participants
- Meeting purpose/agenda
- Key discussion points
- Main outcomes

### 2. Key Decisions
- Decision made
- Context and rationale
- Who decided
- Impact and implications

### 3. Action Items
- Action required
- Owner/responsible person
- Deadline
- Dependencies

### 4. Business Insights
- User needs identified
- Market insights
- Technical constraints
- Opportunities discovered

### 5. Requirements Extracted
- Feature requests
- User stories
- Technical requirements
- Design preferences

### 6. Risk and Issues
- Risks identified
- Issues raised
- Concerns noted
- Mitigation suggestions

## Execution Process

### Step 1: Read and Understand
- Read session notes thoroughly
- Identify structure and content type
- Note key themes and topics

### Step 2: Extract Decisions
- Identify all decisions made
- Extract decision context and rationale
- Note decision makers
- Assess decision impact

### Step 3: Identify Action Items
- List all action items and tasks
- Identify owners and deadlines
- Note dependencies
- Prioritize actions

### Step 4: Extract Business Information
- Capture user needs and pain points
- Note market insights
- Identify requirements
- Document constraints

### Step 5: Document Session
- Create structured session summary
- Organize information by category
- Ensure clarity and completeness
- Link to decision recording if needed

## Deliverables

Primary:
- `projects/[project-name]/05-sessions/YYYYMMDD-[session-name].md`

Supporting:
- `projects/[project-name]/05-sessions/sessions-index.md` (updated)
- `projects/[project-name]/06-decisions/` (if significant decisions made)

## Session Document Template

```markdown
# Session: [Name] - [Date]

## Metadata
- **Date**: YYYY-MM-DD
- **Participants**: [List]
- **Purpose**: [Meeting purpose]

## Summary
[Brief overview of the session]

## Key Discussion Points
1. [Topic 1]
   - [Key points]
2. [Topic 2]
   - [Key points]

## Decisions Made
1. **Decision**: [What was decided]
   - **Context**: [Why this decision]
   - **Decided by**: [Who]
   - **Impact**: [Implications]

## Action Items
- [ ] [Action 1] - Owner: [Name] - Due: [Date]
- [ ] [Action 2] - Owner: [Name] - Due: [Date]

## Requirements Extracted
- [Requirement 1]
- [Requirement 2]

## Insights and Opportunities
- [Insight 1]
- [Opportunity identified]

## Risks and Issues
- **Risk**: [Description] - Mitigation: [Approach]
- **Issue**: [Description] - Action: [Next steps]

## Next Steps
1. [Next step 1]
2. [Next step 2]
```

## Completion Conditions

□ Session notes fully processed
□ All decisions extracted and documented
□ Action items identified with owners
□ Business insights captured
□ Requirements extracted
□ Session summary created
□ Information organized and accessible

## Exit Conditions

□ Session document exists and is complete
□ Decisions recorded (linked to decision-recording.md if significant)
□ Action items tracked
□ Ready to proceed with business planning based on session outcomes
