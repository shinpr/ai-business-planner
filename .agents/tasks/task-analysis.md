# Task Analysis

## Required Rules [MANDATORY - MUST BE ACTIVE]

**RULE AVAILABILITY VERIFICATION:**
1. [VERIFY ACTIVE] `.agents/rules/core/metacognition.md` (loaded at session start)
2. [LOAD IF NOT ACTIVE] `.agents/context-maps/task-rule-matrix.yaml`

**LOADING PROTOCOL:**
- STEP 1: VERIFY metacognition.md is active from initial session setup
- STEP 2: CHECK if task-rule-matrix.yaml is active in working memory
- STEP 3: If task-rule-matrix.yaml NOT active → Execute BLOCKING READ
- STEP 4: CONFIRM all rules active before proceeding with task analysis

**EVIDENCE REQUIRED:**
```
Rule Status Verification:
✓ metacognition.md - ACTIVE (from session setup)
✓ task-rule-matrix.yaml - ACTIVE (loaded/verified)
```

## Purpose

Determine task type, scale, and required resources for business planning activities.

## When to Use

- At the start of any user request
- When task scope is unclear
- When switching to a different type of work

## Completion Conditions

□ Task type identified (business-planning/requirements/prompt-generation/design/session-processing/decision-recording/research/other)
□ Project context understood:
  - Stakeholders identified
  - Market complexity understood
  - Available information assessed
  - User needs clarified
□ Required resources identified:
  - Rules needed
  - External research needed
  - Existing projects to reference (past decisions)
□ Success criteria defined (measurable)
□ Constraints and assumptions documented
□ Workflow confirmed: business-planning-workflow.md for all business planning tasks

## Mandatory Execution Order [STRICT COMPLIANCE REQUIRED]

### Step 0: Initial Setup [BLOCKING - CANNOT SKIP]
If SESSION_BASELINE_DATE not established:
1. [IMMEDIATE] Execute `date` command
2. [STORE] Result as SESSION_BASELINE_DATE for ENTIRE session
3. [ENFORCE] ALL "current/latest/recent" references MUST use SESSION_BASELINE_DATE year

VIOLATION EXAMPLE: Using "2024" in web research when SESSION_BASELINE_DATE shows "2025" = CRITICAL ERROR

### Step 1: Understand Request Essence

- What is the user trying to achieve?
- Is this a new business idea or iterating on existing?
- What stage is this project at (ideation, planning, validation)?

### Step 2: Classify Task Type [REQUIRED]

**Business Planning**: Creating or refining business plan
- New business idea
- Market analysis
- Business model design
- Competitive analysis

**Requirements Definition**: Product/service requirements
- MVP definition
- Core feature identification
- User story creation
- Value proposition clarification

**Prompt Generation**: Prototype generation prompts
- Genspark prompts
- v0 prompts
- Other AI prototyping tools
- Prompt refinement

**Design Specification**: Design requirements
- UI/UX concept
- Design system definition
- Visual requirements
- Brand identity

**Session Processing**: Meeting notes and discussions
- Meeting minutes analysis
- Decision extraction
- Action item identification
- Session summarization

**Decision Recording**: Business decisions
- Go/NoGo decisions
- Strategic choices
- Risk assessments
- Pivot decisions

**Research**: Information gathering
- Market research
- Technology research
- Competitor analysis
- Trend analysis

### Step 3: Understand Context [REQUIRED]

Understand project context:
- Number of stakeholders involved
- Market complexity (niche vs broad)
- Available information (議事録, existing docs, etc.)
- User's specific needs

**Note**: All business planning uses the full workflow regardless of perceived complexity, because business decisions involve people and money.

### Step 4: Execute Rule Selection [BLOCKING CHECKPOINT]

**EXECUTION GATES - System HALTS if any step skipped:**
1. [BLOCKING READ] `task-rule-matrix.yaml` from `.agents/context-maps/`
2. [MANDATORY MATCHING] Task type + scale against matrix
3. [CLASSIFICATION OUTPUT]:
   - Required rules: IMMEDIATE BLOCKING READ
   - Recommended rules: EVALUATE context, then BLOCKING READ if applicable
   - Conditional rules: CHECK conditions, then BLOCKING READ if met
4. [VERIFICATION GATE] CANNOT PROCEED until ALL required rules loaded
5. [PROOF OF COMPLIANCE] Output must list:
   ```
   Rules Successfully Loaded:
   ✓ [filepath] - [reason for loading]
   ✓ [filepath] - [applied to which aspect]
   ```
6. [PLAN INJECTION] IMMEDIATELY inject all identified BLOCKING READs to work plan:
   ```
   [PLAN INJECTION FROM task-analysis - Rule Selection]
   Injected BLOCKING READs from rule selection:
   ✓ [filepath] - required rule
   ✓ [filepath] - conditional rule (condition met)
   ```

### Step 5: Identify Additional Resources

Determine what's needed:
- Which rule files apply
- External research sources (market data, competitor info)
- Reference business plans or templates
- Documentation sources

### Step 6: Define Success Criteria

- Business plan completeness
- Market validation requirements
- Prototype generation success
- Stakeholder approval criteria

### Step 7: Workflow Selection

**For ALL business planning tasks**:
- **ALWAYS use** `business-planning-workflow.md`
- **No exceptions**: Business decisions involve people and money
- **Rationale**: Every business idea requires complete documentation and rigorous evaluation

**Inform user**:
"This is a business planning task. I'll follow the structured workflow (business-planning-workflow.md) to ensure complete documentation and rigorous evaluation, as business decisions involve people and money."

**Then proceed**:
1. Load `.agents/workflows/business-planning-workflow.md`
2. Follow the workflow phases as defined in that file

### Step 8: Mandatory Plan Injection [BLOCKING - AUTOMATIC EXECUTION]

**FOR ALL TASKS WITH BLOCKING READ REQUIREMENTS:**

1. **[SCAN FOR BLOCKING READS]** Identify ALL files requiring BLOCKING READ:
   - From selected workflow (if Standard/Complex scale)
   - From task definitions to be executed
   - From rules that will be loaded

2. **[AUTOMATIC INJECTION]** Add ALL identified BLOCKING READs to work plan:
   ```
   Plan Injection Required:
   □ BLOCKING READ: [file path] - [reason/phase]
   □ BLOCKING READ: [file path] - [reason/phase]
   □ Rule Status Verification after each BLOCKING READ
   ```

3. **[EVIDENCE REQUIRED]** Show plan injection confirmation:
   ```
   [PLAN INJECTION COMPLETED]
   Identified BLOCKING READs from:
   ✓ Workflow phases: [list files]
   ✓ Task definitions: [list files]
   ✓ Required rules: [list files]

   Injected to plan:
   ✓ Total BLOCKING READs: [count]
   ✓ Verification gates: [count]
   ```

4. **[ENFORCEMENT]** CANNOT proceed without:
   - ALL BLOCKING READs identified and injected
   - Plan injection evidence shown above
   - Each BLOCKING READ as explicit task in work plan

**VIOLATION HANDLING:**
- Missing any BLOCKING READ from plan = IMMEDIATE HALT
- Skipping any BLOCKING READ during execution = CRITICAL ERROR
- Proceeding without verification = RETURN TO TASK ANALYSIS

## Deliverables

- Task classification output
- Path recommendation

## Common Patterns

### New Business Idea
1. Identify core problem and solution
2. Estimate market size and target
3. Consider MVP approach
4. Plan validation strategy

### Prototype Generation
1. Ensure requirements are clear
2. Identify design needs (if any)
3. Select appropriate AI tools
4. Plan prompt generation approach

### Decision Documentation
1. Understand decision context
2. Identify stakeholders affected
3. Determine documentation depth
4. Plan follow-up actions

## Decision Tree

**Business-related?**
- YES → Creating new plan?
  - YES: Business Planning task
  - NO → Refining product?
    - YES: Requirements Definition task
    - NO: Generating prototype?
      - YES: Prompt Generation task
      - NO: Design Specification or other
- NO → Processing information?
  - YES: Session Processing or Research task
  - NO → Recording decision?
    - YES: Decision Recording task
    - NO: Other task

## Rule Selection Output Format [SYSTEM VERIFICATION REQUIRED]

### BLOCKING OUTPUT - Cannot proceed without this exact format:
```
[RULE SELECTION CHECKPOINT]
Task Type: [type]
Project Context: [brief context summary]
SESSION_BASELINE_DATE: [stored date from initial setup]

Workflow: business-planning-workflow.md (MANDATORY for all business planning)

Required Rules [BLOCKING READS - MUST BE LOADED]:
✓ [path/to/rule1.md] - LOADED - [applying to: specific aspect]
✓ [path/to/rule2.md] - LOADED - [applying to: specific aspect]

Conditional Rules [LOAD IF CONDITION MET]:
✓ [path/to/rule3.md] - LOADED - [trigger: "design" keyword found in task]
✗ [path/to/rule4.md] - NOT LOADED - [trigger not met: no design requirements]

VERIFICATION: All required rules active in working memory
```

### Rule Loading Strategy [WITH CLEAR TRIGGERS]

**By Task Type [IMMEDIATE LOAD]:**
- Business Planning → ALWAYS: business-model-canvas + value-proposition + market-analysis
- Requirements Definition → ALWAYS: mvp-definition + value-proposition
- Prompt Generation → ALWAYS: prompt-engineering + mvp-definition
- Design Specification → ALWAYS: design-thinking + documentation-criteria
- Session Processing → ALWAYS: documentation-criteria
- Decision Recording → ALWAYS: decision-framework + documentation-criteria
- Research → ALWAYS: market-analysis

**Conditional Loading [LOAD WHEN]:**
- design-thinking → WHEN: "design", "UI", "UX" in requirements OR design specification task
- prompt-engineering → WHEN: "prototype", "genspark", "v0" mentioned OR prompt generation task
- decision-framework → WHEN: "decision", "go/nogo" mentioned

**Universal Loading [ALL BUSINESS PLANNING]:**
- ALL projects → Load full business planning rule set
- NO scale-based variations → Business decisions always require complete evaluation
- ALWAYS load: documentation-criteria + all task-required rules

### Context Optimization [EXPLICIT LOADING CONDITIONS]

**Initial Load [ALWAYS]:**
- Essential rules for identified task type
- Scale-based automatic additions
- NOTE: metacognition.md already active from initial setup

**Trigger-Based Loading [LOAD IMMEDIATELY WHEN]:**
- Market data needed → Load market-analysis
- Design mentioned → Load design-thinking
- Decision point reached → Load decision-framework
- Prototype creation → Load prompt-engineering
- Multiple business models → Load business-model-canvas

**Unloading [AFTER TASK COMPLETE]:**
- Task-specific business patterns
- One-time reference documents
- Completed phase rules

**NEVER UNLOAD:**
- metacognition.md (loaded in initial setup, stays entire session)
- Current task type's essential rules
- documentation-criteria.md (during any documentation task)
