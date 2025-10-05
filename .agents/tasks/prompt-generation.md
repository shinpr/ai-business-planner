# Prompt Generation

## Required Rules [MANDATORY - MUST BE ACTIVE]

**RULE AVAILABILITY VERIFICATION:**
1. [LOAD] `.agents/rules/business/prompt-engineering.md`
2. [LOAD] `.agents/rules/business/mvp-definition.md`
3. [CONDITIONAL LOAD] `.agents/rules/business/design-thinking.md` (if design requirements exist)
4. [VERIFY ACTIVE] `.agents/rules/core/metacognition.md` (from session start)

## Purpose

Generate comprehensive prompts for AI-powered prototype generation tools (Genspark Developer, v0, etc.), incorporating requirements and design specifications.

## Entry Conditions

□ Requirements document exists and approved
□ MVP scope clearly defined
□ Core features identified
□ Design requirements exist (if applicable)
□ All required rules loaded and active

## Prompt Structure (Universal Template)

### 1. Context and Purpose
- Product overview
- Target users
- Core value proposition
- Problem being solved

### 2. MVP Scope and Features
- Explicit MVP definition
- Must Have features listed
- Feature priorities
- Out of scope items

### 3. User Flows
- Primary user journeys
- Key interactions
- Expected user experience

### 4. Functional Specifications
- Detailed feature descriptions
- Specific functionality requirements
- Data requirements
- Integration points (if any)

### 5. Design Requirements (if applicable)
- UI/UX guidelines
- Visual design preferences
- Brand elements
- Accessibility requirements
- Responsive design needs

### 6. Technical Preferences
- Platform (web, mobile, PWA, etc.)
- Technology suggestions (if any)
- Performance expectations
- Browser/device support

### 7. Success Criteria
- What "done" looks like
- Key functionality that must work
- User experience expectations

## Platform-Specific Optimizations

### For Genspark Developer
- Emphasize step-by-step build approach
- Clear feature breakdown
- Specific component requirements
- Integration instructions

### For v0 (Vercel)
- Focus on React components
- Emphasize modern UI/UX
- Tailwind CSS preferences
- Component composition

### For Other AI Tools
- Generic, detailed requirements
- Technology-agnostic descriptions
- Clear success criteria
- Comprehensive feature list

## Execution Process

### Step 0: Interactive Information Gathering [IF NEEDED]

**Context**: This task usually follows requirements and design definition. Most information comes from those documents. However, users may have specific preferences for prototype generation platforms or approaches.

**NO ASSUMPTIONS ALLOWED**: Never infer, guess, or assume platform preferences or prototype details not explicitly provided by the user or documented in previous phases.

**Process**:
1. **Extract existing information** from:
   - Requirements document (primary source)
   - Design document (if exists)
   - Business plan (context)
   - User input and discussions

2. **Identify gaps** in prototype-specific information (see checklist below)

3. **Interactive dialogue with user** (if gaps exist):
   - Ask specific questions for missing information
   - Group questions by category (platform, approach, constraints)
   - Wait for user response before proceeding
   - **NEVER fill gaps with assumptions**

4. **Skip this step if**:
   - Previous documents contain sufficient information
   - No platform-specific preferences needed

**Required Information Checklist** (ask only if missing from previous documents):

**Platform Target** (MUST HAVE):
- [ ] Which AI platform to target? (Genspark, v0, Claude, Cursor, generic)
- [ ] Any platform-specific requirements or constraints?
- [ ] Multiple platforms needed?

**Prototype Approach** (SHOULD HAVE):
- [ ] Prototype fidelity level (low/medium/high)?
- [ ] Key features to prioritize in prototype?
- [ ] Any features to explicitly exclude from prototype?

**Technical Details** (IF APPLICABLE):
- [ ] Technology stack preferences (if not in requirements)?
- [ ] Deployment target (web, mobile, desktop)?
- [ ] Performance or scale requirements for prototype?

**Success Criteria** (SHOULD HAVE):
- [ ] What does a successful prototype look like?
- [ ] Key validation goals for the prototype?

**PROCEED CONDITION**: Platform target confirmed. Other items can default to "best practices for chosen platform"

### Step 1: Requirements Analysis
- Review requirements document thoroughly
- Identify all Must Have features
- Understand user flows
- Note constraints and preferences

### Step 2: Design Integration (if applicable)
- Review design requirements
- Extract key design elements
- Identify UI/UX patterns
- Note brand guidelines

### Step 3: Generic Prompt Creation
- Write comprehensive, platform-agnostic prompt
- Include all sections from template above
- Ensure clarity and specificity
- Make prompt actionable

### Step 4: Platform-Specific Optimization
- Create Genspark-specific prompt
- Create v0-specific prompt
- Create prompts for other tools as needed
- Apply platform best practices

### Step 5: Design Requirements Integration
- If design spec exists, integrate design elements
- Reference design file in prompts
- Include visual requirements
- Specify design system elements

### Step 6: Quality Check
- Prompts are complete and specific
- All requirements reflected
- Design elements integrated (if applicable)
- Platform optimizations applied
- Prompts tested for clarity

## Deliverables

Primary:
- `projects/[project-name]/04-prompts/prototype-prompt.md` (generic)
- `projects/[project-name]/04-prompts/genspark-prompt.md`
- `projects/[project-name]/04-prompts/v0-prompt.md`

Supporting:
- `projects/[project-name]/04-prompts/design-requirements.md` (if applicable)
- `projects/[project-name]/04-prompts/versions/YYYYMMDD-prompt-v1.md`

## Generic Prompt Template

```markdown
# [Product Name] - Prototype Generation Prompt

## Product Overview
[Brief description of the product, its purpose, and core value]

## Target Users
[Primary personas and their needs]

## MVP Scope
[Clear definition of minimum viable product]

## Core Features (Must Have)
1. [Feature 1]
   - Description: [detailed description]
   - User flow: [how users interact]
   - Acceptance criteria: [what success looks like]

2. [Feature 2]
   [...]

## User Flows
### Primary Flow: [Flow Name]
1. [Step 1]
2. [Step 2]
[...]

## Functional Requirements
- [Requirement 1]
- [Requirement 2]
[...]

## Design Requirements (if applicable)
- UI/UX: [guidelines]
- Visual style: [preferences]
- Brand: [elements]
- Responsive: [requirements]

## Technical Preferences
- Platform: [web/mobile/etc]
- Tech stack: [suggestions if any]
- Performance: [expectations]

## Success Criteria
- [Criterion 1]
- [Criterion 2]
[...]

## Out of Scope
- [What NOT to include]
```

## Completion Conditions

□ Generic prompt created and comprehensive
□ Platform-specific prompts generated
□ All MVP features included in prompts
□ User flows clearly described
□ Design requirements integrated (if applicable)
□ Technical preferences specified
□ Success criteria defined
□ Prompts tested for clarity and completeness
□ Prompts actionable for prototype generation

## Common Pitfalls to Avoid

1. **Vague descriptions** → Be specific and detailed
2. **Missing user flows** → Always include key user journeys
3. **Ignoring design** → Integrate design requirements if available
4. **Platform assumptions** → Create generic base, then optimize
5. **Incomplete feature specs** → Include all Must Have details
6. **No success criteria** → Define what "done" means
7. **Overcomplication** → Keep focused on MVP scope

## Quality Gates

Before completion:
- [ ] Generic prompt comprehensive
- [ ] Genspark-specific prompt optimized
- [ ] v0-specific prompt optimized
- [ ] All requirements reflected in prompts
- [ ] Design elements integrated (if applicable)
- [ ] User flows clearly described
- [ ] Success criteria explicit
- [ ] Prompts tested for clarity
- [ ] Platform-specific best practices applied

## Exit Conditions

□ All prompt documents exist and complete
□ All completion conditions satisfied
□ Quality gates passed
□ User approval obtained (STOP POINT in workflow)
□ Prompts ready for prototype generation
