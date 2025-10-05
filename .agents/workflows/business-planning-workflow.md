# Business Planning Workflow

**When to use**: Standard/Complex scale tasks after task-analysis.md recommendation. User approval required before starting.

Track progress internally - do not update this file.

## Workflow Overview

Execute phases sequentially. This workflow covers the core business planning process from business plan creation to prototype prompt generation.

**Note**: Session processing, proposal preparation, and knowledge capture are independent tasks, not part of this core workflow.

## Phase 1: Business Plan Creation

### Pre-Phase Gates [BLOCKING - CANNOT PROCEED WITHOUT]:
1. **[VERIFY PLAN INJECTION]** Confirm work plan contains ALL required BLOCKING READs for this phase
   - If missing any: HALT - Return to task-analysis.md Step 8
2. **[BLOCKING READ]** Execute Read on `.agents/tasks/business-plan-creation.md`
3. **[VERIFY]** business-plan-creation.md is ACTIVE in working memory
4. **[VERIFY]** All rules required by business-plan-creation.md are LOADED (per its Required Rules section)
5. **[CONFIRM]** Entry gates in business-plan-creation.md are satisfied

**ENFORCEMENT**: NO business planning work until business-plan-creation.md confirmed active and Plan Injection verified

### Internal Checklist:
```
□ Past decisions reviewed (if any exist)
□ Executive summary drafted
□ Problem and solution defined
□ Target market identified
□ Personas created
□ Core value proposition articulated
□ Competitive analysis completed
□ Business model designed
□ KPIs/success metrics defined
□ Financial projections (ARR/PL) created
□ Operations plan outlined
□ Risk analysis completed
□ Milestone/roadmap defined
```

### Deliverable:
- Business plan document in `projects/[project-name]/01-planning/business-plan.md`
- Market research in `projects/[project-name]/01-planning/market-research.md`

### Completion Conditions:
- All Tier 1 (MVP-critical) sections complete
- Tier 2 (business viability) sections complete
- Tier 3 (execution details) complete or documented as TBD
- Business value clearly articulated
- Assumptions validated with research
- Past decisions reviewed and learnings applied

### STOP POINT: Business Plan Review [BLOCKING GATE]
**SYSTEM HALT - CANNOT PROCEED WITHOUT:**
1. Business plan document EXISTS at `projects/[project-name]/01-planning/business-plan.md`
2. **[VERIFY COMPLIANCE]** Business plan meets ALL requirements from business-plan-creation.md:
   - All Completion Conditions from business-plan-creation.md satisfied
   - All required sections present (Tier 1, Tier 2 at minimum)
   - Past decisions reviewed and incorporated (if applicable)
   - If non-compliant: REJECT - Return to Phase 1
3. **[EXECUTE REVIEW]** Apply `.agents/tasks/document-review.md` to business plan:
   - Review document quality and completeness
   - Conduct market research and validation
   - Present findings to user
   - Implement approved improvements
   - Create document versions
4. User EXPLICITLY states approval of reviewed document ("yes", "approved", "OK", etc.)

**ENFORCEMENT:**
- NO requirements definition until review complete and approval received
- NO proceeding without full task definition compliance
- VIOLATION = Return to business plan phase

## Phase 2: Requirements Definition

### Pre-Phase Gates [BLOCKING - CANNOT PROCEED WITHOUT]:
1. **[VERIFY PLAN INJECTION]** Confirm work plan contains ALL required BLOCKING READs for this phase
   - If missing any: HALT - Return to task-analysis.md Step 8
2. **[BLOCKING READ]** Execute Read on `.agents/tasks/requirements-definition.md`
3. **[VERIFY]** requirements-definition.md is ACTIVE in working memory
4. **[VERIFY]** All rules required by requirements-definition.md are LOADED
5. **[VERIFY]** Business plan from Phase 1 EXISTS and has been APPROVED
6. **[CONFIRM]** Entry gates in requirements-definition.md are satisfied

**ENFORCEMENT**: NO requirements work until requirements-definition.md confirmed active and Plan Injection verified

### Internal Checklist:
```
□ Core value extracted from business plan
□ MVP scope defined
□ Core features identified and prioritized (MoSCoW)
□ User stories created
□ Technical requirements outlined
□ Non-functional requirements documented
□ Constraints identified
□ Success criteria defined
□ Validation hypotheses formulated
```

### Deliverable:
- Requirements document in `projects/[project-name]/02-requirements/requirements.md`
- Core value definition in `projects/[project-name]/02-requirements/core-value.md`

### Completion Conditions:
- MVP clearly defined
- All core features specified
- Requirements traceable to business plan
- Validation approach documented

### STOP POINT: Requirements Review [BLOCKING GATE]
**SYSTEM HALT - CANNOT PROCEED WITHOUT:**
1. Requirements document EXISTS at `projects/[project-name]/02-requirements/requirements.md`
2. **[VERIFY COMPLIANCE]** Requirements meet ALL requirements from requirements-definition.md
3. **[EXECUTE REVIEW]** Apply `.agents/tasks/document-review.md` to requirements:
   - Review document quality and completeness
   - Verify traceability to business plan
   - Present findings to user
   - Implement approved improvements
   - Create document versions
4. User EXPLICITLY states approval of reviewed document
5. MVP scope is clear and achievable

**ENFORCEMENT:**
- NO design or prompt generation until review complete and approval received
- VIOLATION = Return to requirements phase

## Phase 3: Design Specification (Conditional - User Decision Required)

**Execute this phase based on user decision**

### STOP POINT: Design Decision [BLOCKING GATE]
**SYSTEM HALT - MUST ASK USER:**
1. **[ASK USER]** "Do you need design specifications for this prototype? Design specs include UI/UX concept, visual design (colors, typography), brand identity, and accessibility requirements. [Y/n]"
2. **If YES**: Proceed with design specification below
3. **If NO**: Document decision as "Design: Using default AI tool designs" and skip to Phase 4

### Pre-Phase Gates [BLOCKING - ONLY IF USER SAID YES]:
1. **[VERIFY PLAN INJECTION]** Confirm work plan contains ALL required BLOCKING READs for this phase
2. **[BLOCKING READ]** Execute Read on `.agents/tasks/design-specification.md`
3. **[VERIFY]** design-specification.md is ACTIVE in working memory
4. **[VERIFY]** All rules required by design-specification.md are LOADED
5. **[VERIFY]** Requirements from Phase 2 EXISTS and has been APPROVED
6. **[CONFIRM]** Entry gates in design-specification.md are satisfied

### Internal Checklist:
```
□ UI/UX concept defined
□ Design system specified
□ Visual requirements documented
□ Brand identity considered
□ Design assets identified
□ Accessibility requirements noted
```

### Deliverable:
- Design requirements in `projects/[project-name]/03-design/design-requirements.md`
- UI concept in `projects/[project-name]/03-design/ui-concept.md`
- Design assets in `projects/[project-name]/03-design/assets/`

### Completion Conditions:
- Design vision clear
- Requirements sufficient for prototype generation
- Consistent with brand/product vision

### STOP POINT: Design Review [BLOCKING GATE - ONLY IF DESIGN CREATED]
**SYSTEM HALT - CANNOT PROCEED WITHOUT:**
1. Design documents EXIST in `projects/[project-name]/03-design/`
2. **[VERIFY COMPLIANCE]** Design meets ALL requirements from design-specification.md
3. **[EXECUTE REVIEW]** Apply `.agents/tasks/document-review.md` to design specification:
   - Review document quality and completeness
   - Verify alignment with requirements and brand
   - Present findings to user
   - Implement approved improvements
   - Create document versions
4. User EXPLICITLY states approval of reviewed document

## Phase 4: Prompt Generation

### Pre-Phase Gates [BLOCKING - CANNOT PROCEED WITHOUT]:
1. **[VERIFY PLAN INJECTION]** Confirm work plan contains ALL required BLOCKING READs for this phase
2. **[BLOCKING READ]** Execute Read on `.agents/tasks/prompt-generation.md`
3. **[VERIFY]** prompt-generation.md is ACTIVE in working memory
4. **[VERIFY]** All rules required by prompt-generation.md are LOADED
5. **[VERIFY]** Requirements from Phase 2 EXISTS and has been APPROVED
6. **[CHECK]** Design requirements from Phase 3 EXISTS (if user chose to create design)
7. **[CONFIRM]** Entry gates in prompt-generation.md are satisfied

**ENFORCEMENT**: NO prompt generation until prompt-generation.md confirmed active and Plan Injection verified

### Internal Checklist:
```
□ Generic prototype prompt created
□ Platform-specific prompts generated (Genspark, v0, etc.)
□ Design requirements integrated (if applicable)
□ Technical requirements included
□ User flows specified
□ Expected functionality documented
□ Success criteria for prototype defined
```

### Deliverable:
- Generic prompt in `projects/[project-name]/04-prompts/prototype-prompt.md`
- Platform-specific prompts (e.g., `genspark-prompt.md`, `v0-prompt.md`)
- Design requirements file (if applicable) referenced in prompts

### Completion Conditions:
- Prompts are complete and actionable
- All requirements reflected in prompts
- Platform-specific optimizations applied
- Prompts tested (if possible) or validated

### STOP POINT: Prompt Review [BLOCKING GATE]
**SYSTEM HALT - CANNOT PROCEED WITHOUT:**
1. Prompt documents EXIST in `projects/[project-name]/04-prompts/`
2. **[VERIFY COMPLIANCE]** Prompts meet ALL requirements from prompt-generation.md
3. **[EXECUTE REVIEW]** Apply `.agents/tasks/document-review.md` to prompts:
   - Review prompt quality and completeness
   - Verify all requirements included
   - Check platform-specific optimizations
   - Present findings to user
   - Implement approved improvements
   - Create document versions
4. User EXPLICITLY states approval of reviewed document
5. Prompts are ready for prototype generation

**ENFORCEMENT:**
- NO prototype generation until review complete and approval received
- VIOLATION = Return to prompt generation phase

## Workflow Completion

### Final Deliverables:
- Complete business plan (`01-planning/`)
- Product requirements (`02-requirements/`)
- Design specifications (`03-design/`) - if created
- Prototype generation prompts (`04-prompts/`)

### Post-Workflow Activities (Independent Tasks):
These are NOT part of this workflow but can be used as needed:

- **Proposal Preparation** (`.agents/tasks/proposal-preparation.md`): Create presentation materials when needed
- **Session Processing** (`.agents/tasks/session-processing.md`): Process meeting notes anytime
- **Decision Recording** (`.agents/tasks/decision-recording.md`): Record Go/NoGo and other decisions
- **Knowledge Capture**: Review and organize project learnings

### Success Criteria:
- All phases completed (or Design explicitly skipped by user)
- All deliverables created and approved
- Documentation organized in project directory
- Ready for prototype generation or next steps
