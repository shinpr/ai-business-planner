# AGENTS.md - 事業計画エージェント

## ABSOLUTE PRINCIPLES

1. **EXECUTE all rules and requirements in task/rule files - no exceptions**
2. **COMPLETE all entry and exit conditions for every task**
3. **STOP at gates - proceed only when conditions are met**

## Initial Setup [FIRST TIME ONLY]

**Complete before any other operation:**
1. Execute `date` command → Store as SESSION_BASELINE_DATE
2. Apply `.agents/rules/core/metacognition.md` → Keep active entire session
3. Use SESSION_BASELINE_DATE for all date references (web search, docs, etc.)
4. Verify project structure with `ls -la`

## Core Execution Principle

**Universal Entry Point**: Every request starts with task-analysis.md to determine the appropriate path.

## Task Analysis - Required First Step

**ALWAYS start here for any user request:**
1. Apply `.agents/tasks/task-analysis.md`
2. Determine task type and scale with evidence
3. Use `.agents/context-maps/task-rule-matrix.yaml` to identify required rules
4. Based on analysis results, choose appropriate path:

### Path Selection Based on Task Analysis

**For ALL Business Planning Tasks:**
- **ALWAYS use** business-planning-workflow.md
- **No exceptions**: Business decisions involve people and money
- **Full documentation required**: Every project gets complete evaluation

**Rationale**:
- New businesses and products involve significant decisions with real consequences
- Every idea deserves rigorous evaluation regardless of perceived simplicity
- Complete documentation enables learning from past decisions

**For Other Task Types** (session processing, decision recording, proposal prep):
- Execute specific task definition directly
- These are independent tasks, not part of core workflow

## Core Principles

### Language Strategy [MANDATORY]
**Internal processing in English, user-facing content in Japanese:**
- **Internal operations** (thinking, rule interpretation, analysis, tool usage): Execute in English
- **User interaction** (conversation, responses, questions): Communicate in Japanese
- **Deliverables** (business plans, requirements, prompts, documentation): Write in Japanese
- **Rationale**: AI models achieve highest precision with English for reasoning; this maximizes accuracy while ensuring Japanese outputs for stakeholders

### Plan Injection [MANDATORY ENFORCEMENT]
**All tasks require Plan Injection for BLOCKING READs:**
- Task-analysis.md Step 8 scans and identifies ALL BLOCKING READ requirements
- Work plans MUST contain every BLOCKING READ from workflow/tasks/rules
- Each phase verifies its BLOCKING READs are in the plan
- Gates verify Plan Injection evidence before proceeding
- Missing ANY BLOCKING READ = IMMEDIATE HALT

### Task Definition Loading
**Task definitions define WHAT to build - never skip them:**
- Verify entry gates before proceeding
- Follow Required Rules section in each task definition

### Rule Application
**Apply rules based on task type from task-analysis:**
- Rules are loaded progressively as needed
- Each task definition specifies its required rules
- Unload task-specific rules after completion

### Quality Standards
**Before marking any task complete:**
- All deliverables created (business plan, requirements, prompts, etc.)
- All quality checks satisfied
- Task exit conditions are satisfied
- Work documented as needed

## Approval Points

**Principle**: Get user approval at significant milestones.

Common approval points:
- When recommending a workflow for Standard/Complex tasks
- After creating business plan or requirements documents
- After generating prototype prompts
- When business approach changes significantly
- At task definition specified stop points

**VIOLATIONS TO PREVENT:**
- Work plan without ALL BLOCKING READs = RETURN TO TASK ANALYSIS
- Skipping ANY BLOCKING READ = IMMEDIATE HALT
- Proceeding without task definition compliance = BLOCKING ERROR

## Quality Standards

**Universal quality requirements:**
- Follow documented business frameworks (BMC, Value Proposition Canvas, etc.)
- All deliverables must be complete and well-structured
- Follow standards defined in business-specific rules
- Each task definition specifies its quality gates

## Metacognition Checkpoints

Perform self-assessment at these mandatory points:
- Task type changes
- Unexpected issues occur
- Completing a meaningful unit of work
- Before starting new phase
- After completing each task from work plan

## Context Management

**Guidelines**:
- Load rules progressively, not all at once
- Unload task-specific rules after completion
- Keep only frequently-used rules loaded
- If context feels constrained, ask user for cleanup guidance

## Error Recovery

When stuck or encountering errors:
1. Re-read current task definition
2. Check if required rules are loaded
3. Look for common pitfalls in business planning
4. If unable to resolve, ask user for clarification

## File Organization

**Tasks** (.agents/tasks/):
- task-analysis.md: **Entry point**
- business-plan-creation.md: Business plan generation
- requirements-definition.md: Product requirements definition
- prompt-generation.md: Prototype prompt generation
- design-specification.md: Design requirements (optional)
- session-processing.md: Meeting notes and session processing
- decision-recording.md: Decision documentation
- proposal-preparation.md: Proposal and presentation prep

**Workflows** (.agents/workflows/):
- business-planning-workflow.md: Standard/Complex scale workflow

**Context Maps** (.agents/context-maps/):
- task-rule-matrix.yaml: Task-to-rule mappings

**Core Rules** (.agents/rules/core/):
- metacognition.md: Self-assessment
- documentation-criteria.md: Documentation criteria

**Business Rules** (.agents/rules/business/):
- business-model-canvas.md: Business Model Canvas framework
- value-proposition.md: Value Proposition Canvas
- market-analysis.md: Market research and competitive analysis
- mvp-definition.md: MVP definition methodologies
- prompt-engineering.md: Prompt engineering for prototypes
- design-thinking.md: Design thinking methodologies
- decision-framework.md: Decision-making frameworks

## Anti-Patterns to Avoid

1. **Skipping task-analysis.md** → ALWAYS start with task analysis
2. **Loading all rules upfront** → Load progressively based on task needs
3. **Ignoring task entry/exit conditions** → Verify gates at each step
4. **Working without task definitions** → Task definitions define WHAT to build
5. **Assuming workflow is always needed** → Simple tasks can use direct task definitions
6. **Premature workflow selection** → Let task-analysis determine the approach
7. **Creating business plans without market research** → Always validate assumptions
8. **Generating prompts without requirements** → Requirements must come first

## Success Metrics

Track internally:
- Task completion rate
- Rules actually used vs loaded
- Quality checks passing rate (should be 100%)
- Appropriate path selection (direct vs workflow)
- Business plan quality and completeness
- Prototype prompt effectiveness

## Project Organization

All project deliverables are stored in `projects/[project-name]/`:
- `01-planning/`: Business plans and market research
- `02-requirements/`: Product requirements and MVP definition
- `03-design/`: Design requirements (optional)
- `04-prompts/`: Prototype generation prompts
- `05-sessions/`: Meeting notes and session records
- `06-decisions/`: Decision logs and Go/NoGo records
- `07-artifacts/`: Prototypes, presentations, research materials
