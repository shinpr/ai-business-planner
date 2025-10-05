# Requirements Definition

## Required Rules [MANDATORY - MUST BE ACTIVE]

**RULE AVAILABILITY VERIFICATION:**
1. [LOAD] `.agents/rules/business/mvp-definition.md`
2. [LOAD] `.agents/rules/business/value-proposition.md`
3. [LOAD] `.agents/rules/core/documentation-criteria.md`
4. [VERIFY ACTIVE] `.agents/rules/core/metacognition.md` (from session start)

## Purpose

Define product/service requirements based on business plan, focusing on MVP and core value delivery for prototype generation.

## Entry Conditions

□ Business plan exists and has been approved
□ Core value proposition clearly defined in business plan
□ Target market and personas identified
□ All required rules loaded and active

## Requirements Document Structure

### 1. Core Value Definition
- Extract and refine core value from business plan
- User pain points addressed
- Key benefits delivered
- Success criteria for value delivery

### 2. MVP Scope
- Minimum viable product definition
- Core hypothesis to validate
- Success metrics for MVP
- Out of scope (explicitly)

### 3. Feature Prioritization (MoSCoW)
**Must Have** (Core Features):
- Critical for MVP
- Directly deliver core value
- User cannot use product without these

**Should Have** (Important Features):
- Important but not critical for MVP
- Enhance user experience
- Can be added post-MVP

**Could Have** (Nice to Have):
- Desirable but not essential
- Future enhancements
- Low priority

**Won't Have** (Out of Scope):
- Explicitly excluded from current scope
- Potential future consideration

### 4. User Stories
- As a [persona], I want to [action] so that [benefit]
- Acceptance criteria for each story
- Priority mapping to MoSCoW

### 5. Functional Requirements
- Core functionality description
- User flows and interactions
- Data requirements
- Integration points (if any)

### 6. Non-Functional Requirements
- Performance expectations
- Usability requirements
- Accessibility needs
- Security considerations (basic)
- Scalability considerations (basic)

### 7. Technical Requirements (High-Level)
- Platform preferences (web, mobile, etc.)
- Technology constraints
- Integration requirements
- Data storage needs

### 8. Constraints and Assumptions
- Business constraints
- Technical constraints
- Time/resource constraints
- Key assumptions to validate

### 9. Validation Approach
- How to validate MVP hypothesis
- Key metrics to measure
- User feedback approach
- Success/failure criteria

## Execution Process

### Step 0: Interactive Information Gathering [IF NEEDED]

**Context**: This task usually follows business plan creation. Most information comes from the business plan. However, users may need to provide additional details.

**NO ASSUMPTIONS ALLOWED**: Never infer, guess, or assume information not explicitly provided by the user or documented in the business plan.

**Process**:
1. **Extract existing information** from:
   - Business plan (primary source)
   - User input and discussions
   - Provided documents (if any)

2. **Identify gaps** in required information (see checklist below)

3. **Interactive dialogue with user** (if gaps exist):
   - Ask specific questions for missing information
   - Group questions by category (features, users, constraints, etc.)
   - Wait for user response before proceeding
   - **NEVER fill gaps with assumptions**

4. **Skip this step if**:
   - Business plan contains all needed information
   - No additional clarification needed

**Required Information Checklist** (ask only if missing from business plan):

**MVP Features** (MUST HAVE):
- [ ] Core features list (from business plan)
- [ ] Any additional features user wants to consider?
- [ ] Any features explicitly excluded?

**User Experience** (SHOULD HAVE):
- [ ] Key user flows (happy path)
- [ ] Critical interactions
- [ ] Accessibility requirements (if any)

**Technical Constraints** (SHOULD HAVE):
- [ ] Platform requirements (web/mobile/desktop)
- [ ] Technology preferences or restrictions
- [ ] Integration requirements
- [ ] Data/privacy requirements

**Success Criteria** (MUST HAVE):
- [ ] How to measure MVP success (beyond business plan KPIs)?
- [ ] Validation approach (user testing, beta, etc.)

**PROCEED CONDITION**: All MUST HAVE items confirmed or marked as "TBD - to be determined during design phase"

### Step 1: Extract Core Value
- Review business plan thoroughly
- Identify the essential value proposition
- Define what makes this product unique and valuable
- Map value to user needs

### Step 2: Define MVP Scope
- Apply mvp-definition.md methodologies
- Identify minimum feature set for value delivery
- Define validation hypothesis
- Set success criteria

### Step 3: Prioritize Features
- List all potential features
- Apply MoSCoW prioritization
- Focus on "Must Have" for MVP
- Document rationale for priorities

### Step 4: Create User Stories
- Write user stories for all Must Have features
- Add Should Have stories for context
- Include acceptance criteria
- Ensure stories are testable

### Step 5: Document Requirements
- Write comprehensive requirements document
- Include all sections above
- Ensure traceability to business plan
- Make requirements actionable for prototype generation

### Step 6: Quality Check
- All Must Have features identified
- Requirements clear and specific
- Traceability to business value maintained
- Ready for design and prompt generation

## Deliverables

Primary:
- `projects/[project-name]/02-requirements/requirements.md`
- `projects/[project-name]/02-requirements/core-value.md`

Supporting:
- `projects/[project-name]/02-requirements/versions/YYYYMMDD-requirements-v1.md`

## Completion Conditions

□ Core value clearly extracted and refined
□ MVP scope precisely defined
□ All features prioritized with MoSCoW
□ User stories created for core features
□ Functional requirements documented
□ Non-functional requirements identified
□ Technical requirements outlined
□ Constraints and assumptions explicit
□ Validation approach defined
□ Document traces back to business plan
□ Requirements actionable for prototype creation

## Common Pitfalls to Avoid

1. **Scope creep** → Strictly maintain MVP focus
2. **Vague requirements** → Be specific and measurable
3. **Missing validation criteria** → Define how to measure success
4. **Ignoring constraints** → Explicitly document limitations
5. **Feature dumping** → Prioritize ruthlessly using MoSCoW
6. **Disconnected from business plan** → Maintain traceability
7. **Overly technical** → Keep requirements user-centric

## Quality Gates

Before completion:
- [ ] Core value statement clear and compelling
- [ ] MVP scope minimal but complete
- [ ] Must Have features truly essential
- [ ] User stories well-formed with acceptance criteria
- [ ] Requirements specific and testable
- [ ] Non-functional requirements considered
- [ ] Validation approach practical
- [ ] Document professional and complete

## Exit Conditions

□ Requirements document exists and is complete
□ All completion conditions satisfied
□ Quality gates passed
□ User approval obtained (STOP POINT in workflow)
□ Ready to proceed to design specification or prompt generation
