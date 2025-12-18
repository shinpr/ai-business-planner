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

### 2.5. Prototype Scope Limitations [CRITICAL]

**INCLUDE in prototype prompts:**
- UI/UX specifications (layout, components, interactions)
- User flows (step-by-step journeys)
- Visual design (colors, fonts, spacing)
- Mock data examples (simple JSON structures)

**Prototype Alternatives** (server/database requirements → frontend equivalents):
- Backend implementation → Use LocalStorage or hardcoded arrays
- Database schemas → Define simple JSON structures for mock data
- API endpoints → Use static mock responses
- Authentication → Use mock login state (boolean flag)
- Third-party APIs → Use placeholder data representing expected responses
- Infrastructure/deployment → Focus on client-side behavior only

**Decision Rule**: Requires server/database? → Replace with frontend mock equivalent above.

### 2.6. Output Format Principle [CRITICAL]

**Purpose**: Separate machine-executable prompts from human-readable guidance to prevent confusion and ensure clean, copy-pasteable prompts.

**File Separation Strategy**:
Generate TWO distinct files per platform:
1. **Prompt file** (`[platform]-prompt.md`): Machine-executable instructions only
2. **Guide file** (`[platform]-guide.md`): Human-readable usage documentation

**Prompt File Content (what to INCLUDE)**:
- Direct instructions for the AI tool to execute
- Content that users will copy-paste verbatim into the AI platform
- Specifications, requirements, and technical details
- Examples and mock data that the AI tool should use

**Human Guidance Content → Move to guide file**:
- Platform introductions/descriptions → `[platform]-guide.md`
- Usage instructions for the AI tool → `[platform]-guide.md`
- Post-execution workflows → `[platform]-guide.md`
- Best practices/troubleshooting → `[platform]-guide.md`
- Editorial commentary → `[platform]-guide.md`

**Guide File Content (what to INCLUDE)**:
- Platform introduction and capabilities
- How to access and use the platform
- Step-by-step usage instructions
- Best practices and optimization tips
- Troubleshooting common issues
- Recommended workflows
- Examples of iterative improvements
- Integration and deployment guidance

**Decision Test** (apply to each section before writing):
```
Question: "Would I paste this text directly into the AI tool for execution?"

YES → Include in [platform]-prompt.md
NO  → Include in [platform]-guide.md (if useful for humans)
```

**Anti-Pattern Example**:
```markdown
## About v0 (Vercel) [WRONG - meta-information about platform]
v0 is an AI-powered UI generator provided by Vercel.

## How to Use v0 [WRONG - usage instructions]
1. Access v0.dev
2. Enter your prompt

## Recommended Workflow [WRONG - post-execution guidance]
1. Generate with v0
2. Integrate into Next.js
3. Deploy to Vercel
```

**Correct Pattern**:
All above content → `v0-guide.md`
Pure prompt specifications → `v0-prompt.md`

**Enforcement**: Before completing this task, verify that ALL generated prompt files contain ONLY content that passes the Decision Test.

### 3. User Flows
- Primary user journeys
- Key interactions
- Expected user experience

### 4. Functional Specifications
- Detailed feature descriptions
- Specific functionality requirements
- Data requirements
- Integration points (if any)

### 5. Design Requirements

When design specification exists:
- Atmosphere keywords and translated design elements
- Color palette with hex values
- Override instructions for UI library defaults
- Elements to avoid

When design specification does not exist:
- Extract industry characteristics from business plan
- Define minimal atmosphere direction

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

**IMPORTANT**: These sections provide platform-specific guidance.
During execution, ask user which platform(s) to target and generate optimized prompts accordingly.

### General Prototype Guidelines (All Platforms)
- Focus on UI/UX with mock data
- Apply principles from `.agents/rules/business/prompt-engineering.md`

---

### For Genspark Developer
**Credit Awareness:**
- Free tier: ~200 credits/day
- Keep prompts under 1000 lines

**Apply:** Genspark section in `prompt-engineering.md`

---

### For v0 (Vercel)

**Apply:** v0 section in `prompt-engineering.md`

---

### For Other AI Tools

**Apply:** General AI Tools section in `prompt-engineering.md`

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
- [ ] Which AI platform(s) to target? Options:
  - Genspark Developer
  - v0 (Vercel)
  - Generic (platform-agnostic)
  - Multiple platforms (specify which)
- [ ] Generate prompts for:
  - Single platform only (recommended - optimized output)
  - Multiple platforms (generic + platform-specific variants)
- [ ] Any platform-specific constraints? (e.g., Genspark credit budget)

**Recommendation**: Choose single platform for focused optimization.
Generate platform-specific prompt using guidelines from Section "Platform-Specific Optimizations".

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

### Step 2: Design Integration

If design specification exists:
- Extract atmosphere keywords and design translations
- Confirm color palette with hex values
- Identify required UI library overrides

If design specification does not exist:
- Extract industry characteristics from business plan
- Set minimal atmosphere keywords

### Step 3: Generic Prompt Creation
- Write comprehensive, platform-agnostic prompt
- Include all sections from template above
- Ensure clarity and specificity
- Make prompt actionable

### Step 4: Platform-Specific Optimization
**Based on user's platform choice from Step 0:**

- If single platform chosen:
  - Create ONE optimized prompt for that platform
  - Apply platform-specific best practices from Section "Platform-Specific Optimizations"
  - Include platform-specific constraints (e.g., Genspark credit limits)

- If multiple platforms chosen:
  - Create generic base prompt
  - Create platform-specific variants as needed
  - Apply optimizations per platform guidelines

- Always apply prototype scope limitations (Section 2.5)

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

**CRITICAL**: Generate separate prompt and guide files per Section 2.6 Output Format Principle.

**For single platform:**
- `projects/[project-name]/04-prompts/[platform]-prompt.md` (machine-executable only)
- `projects/[project-name]/04-prompts/[platform]-guide.md` (human usage documentation)

**For multiple platforms:**
- `projects/[project-name]/04-prompts/[platform1]-prompt.md` (e.g., `genspark-prompt.md`)
- `projects/[project-name]/04-prompts/[platform1]-guide.md` (e.g., `genspark-guide.md`)
- `projects/[project-name]/04-prompts/[platform2]-prompt.md` (e.g., `v0-prompt.md`)
- `projects/[project-name]/04-prompts/[platform2]-guide.md` (e.g., `v0-guide.md`)

**Supporting files (always):**
- `projects/[project-name]/04-prompts/design-requirements.md` (if design spec exists)
- `projects/[project-name]/04-prompts/versions/YYYYMMDD-[platform]-prompt-v1.md`

**File Content Verification**:
Before writing each file, apply the Decision Test from Section 2.6:
- Prompt files: Only content that would be pasted directly into AI tool
- Guide files: Only content that explains usage to humans

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

## Design Requirements

### Atmosphere
- Keywords: [3-5 adjectives]
- Avoid: [elements]

### Visual Specifications
- Colors: Primary #[hex], Secondary #[hex], Accent #[hex]
- Border-radius: [direction]
- Shadows: [direction]
- Spacing: [direction]

### UI Library Overrides
[Platform-specific override instructions]

### Responsive
- [requirements]

## Technical Preferences
- Platform: [web/mobile/etc]
- Tech stack: [suggestions if any]
- Performance: [expectations]

## Success Criteria
- [Criterion 1]
- [Criterion 2]
[...]

## Scope Boundaries
- [Explicit limits of this prototype]
```

## Completion Conditions

□ Prompt files contain only machine-executable content (passed Decision Test)
□ Guide files contain only human-readable documentation
□ Platform-specific prompts generated per platform choice
□ All MVP features included in prompt files
□ User flows clearly described in prompts
□ Design requirements integrated (if applicable)
□ Atmosphere reflected as concrete design elements
□ UI library override instructions included (for v0/Genspark)
□ Success criteria defined in prompts
□ Prompts ready for direct copy-paste into AI tools

## Common Pitfalls to Avoid

1. **Mixing prompt and guide content** → CRITICAL: Apply Decision Test strictly
2. **Including usage instructions in prompts** → Move to guide files
3. **Vague descriptions** → Be specific and detailed
4. **Missing user flows** → Always include key user journeys
5. **Ignoring design** → Integrate design requirements if available
6. **Platform assumptions** → Create generic base, then optimize
7. **Incomplete feature specs** → Include all Must Have details
8. **No success criteria** → Define what "done" means
9. **Overcomplication** → Keep focused on MVP scope

## Quality Gates

Before completion:
- [ ] **CRITICAL**: All prompt files pass Decision Test (executable content only)
- [ ] **CRITICAL**: Guide files separated from prompt files
- [ ] Platform-specific prompts optimized per platform
- [ ] All requirements reflected in prompt files
- [ ] User flows clearly described in prompts
- [ ] Success criteria explicit in prompts
- [ ] Platform-specific best practices from `prompt-engineering.md` applied

## Exit Conditions

□ All prompt files pass Decision Test
□ All guide files created with usage documentation
□ All quality gates passed
□ User approval obtained (STOP POINT in workflow)
