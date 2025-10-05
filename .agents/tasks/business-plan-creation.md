# Business Plan Creation

## Required Rules [MANDATORY - MUST BE ACTIVE]

**RULE AVAILABILITY VERIFICATION:**
1. [LOAD] `.agents/rules/core/documentation-criteria.md`
2. [LOAD] `.agents/rules/business/business-model-canvas.md`
3. [LOAD] `.agents/rules/business/value-proposition.md`
4. [LOAD] `.agents/rules/business/market-analysis.md`
5. [VERIFY ACTIVE] `.agents/rules/core/metacognition.md` (from session start)

## Purpose

Create comprehensive business plan for new product/service, incorporating market analysis, business model, and execution strategy.

## Entry Conditions

□ Project context understood (from task-analysis or session-processing)
□ Business idea or problem statement provided
□ Target market information available (or to be researched)
□ All required rules loaded and active

## Business Plan Structure (Based on Tier System)

### Tier 1: Prototype-Critical (MUST HAVE)
1. **Executive Summary** (1-2 pages)
   - Business concept overview
   - Value proposition summary
   - Target market snapshot
   - Key differentiators

2. **Problem and Solution**
   - Problem statement with evidence
   - Proposed solution
   - Why now? (market timing)

3. **Target Market and Personas**
   - Market segmentation
   - Persona definitions (2-3 primary personas)
   - Market size estimation

4. **MVP Definition and Core Features**
   - Minimum viable product scope
   - Core features (Must-Have using MoSCoW)
   - User value delivery

5. **Product Core Value**
   - Unique value proposition
   - Key benefits and differentiation
   - User pain points addressed

6. **Competitive Analysis and Differentiation**
   - Direct and indirect competitors
   - Competitive positioning
   - Unique advantages

### Tier 2: Business Viability (SHOULD HAVE)
7. **Business Model**
   - Revenue streams
   - Pricing strategy
   - Cost structure overview

8. **Go-to-Market Strategy**
   - Marketing channels
   - Sales approach
   - Customer acquisition plan

9. **KPIs and Success Metrics**
   - Key performance indicators
   - Success criteria
   - Measurement approach

10. **Milestones and Roadmap**
    - 3-6-12 month milestones
    - Product development timeline
    - Business development timeline

### Tier 3: Execution Details (COULD HAVE)
11. **Financial Projections**
    - ARR/PL plan
    - Revenue projections
    - Cost projections
    - Break-even analysis

12. **Operations Plan**
    - Customer support approach
    - Billing/payment process
    - Contract management

13. **Team and Organization**
    - Current team
    - Key roles needed
    - Hiring plan

14. **Risk Analysis**
    - Technical risks
    - Market risks
    - Competitive risks
    - Mitigation strategies
    - Legal/regulatory considerations

15. **Future Product Vision**
    - Long-term vision (1-3 years)
    - Expansion opportunities
    - Platform evolution

## Execution Process

### Step 1: Interactive Information Gathering [MANDATORY DIALOGUE]

**NO ASSUMPTIONS ALLOWED**: Never infer, guess, or assume information not explicitly provided by the user. This prevents misalignment and ensures accurate documentation.

**Process**:
1. **Extract existing information** from:
   - User input and discussions
   - Provided documents (if any)
   - Past project decisions (if applicable)

2. **Identify required information** using checklist below

3. **Interactive dialogue with user**:
   - Ask specific questions for each missing piece of information
   - Present questions clearly and grouped by category
   - Wait for user response before proceeding
   - **NEVER fill gaps with assumptions or inferences**

4. **Web research** (only when):
   - User explicitly requests research ("please research...", "look up...")
   - During review phase (see Step 5: Quality Check & Research)
   - Not during initial information gathering

**Required Information Checklist**:

**Business Basics** (MUST HAVE):
- [ ] Business idea/concept description
- [ ] Problem being solved
- [ ] Target users/customers (who specifically?)
- [ ] Proposed solution approach
- [ ] Core value proposition (why would users choose this?)

**Market Context** (MUST HAVE):
- [ ] Target market definition
- [ ] Market size estimation (or user's hypothesis)
- [ ] Key competitors (if known by user)
- [ ] Unique differentiators

**MVP Scope** (MUST HAVE):
- [ ] Core features (must-have for first version)
- [ ] Success metrics/KPIs
- [ ] Timeline expectations (if any)

**Business Model** (SHOULD HAVE):
- [ ] Revenue model (how will it make money?)
- [ ] Pricing strategy (if applicable)
- [ ] Cost structure (major cost drivers)
- [ ] Customer acquisition approach

**STOP CONDITION**: Only proceed to Step 1.5 when all MUST HAVE items are confirmed with user. For SHOULD HAVE items, note as "TBD - to be determined in later phases" if user doesn't have answers.

### Step 1.5: Past Decisions Review [MANDATORY]
**Purpose**: Learn from past business planning efforts to improve current plan.

**Execution**:
1. Search for past decision records:
   ```bash
   find projects/*/06-decisions/ -name "*.md" -type f 2>/dev/null
   ```

2. If past decisions exist:
   - **Read and analyze** all decision documents
   - **Extract learnings**:
     - What worked well?
     - What didn't work?
     - What assumptions were wrong?
     - What market insights were gained?
     - What risks materialized?
   - **Identify patterns**:
     - Common success factors
     - Repeated mistakes
     - Market trends validation
     - Customer feedback themes

3. **Feedback to user**:
   - "I found [N] past business decisions in your projects."
   - "Key learnings:"
     - Learning 1: [Description]
     - Learning 2: [Description]
   - "Recommendations for current plan:"
     - Recommendation 1: [Based on past learning]
     - Recommendation 2: [Avoid past mistake]

4. **Apply learnings** to current business plan:
   - Incorporate validated assumptions
   - Avoid previously identified pitfalls
   - Build on successful strategies
   - Address recurring concerns

5. If no past decisions found:
   - Note: "This is your first project in this system. Proceeding with standard business planning."
   - Continue to Step 2

**Why This Matters**:
Each business plan captured in this repository improves the quality of future plans. Past Go/NoGo decisions contain invaluable insights about what makes a business viable.

### Step 2: Business Model Design
- Apply business-model-canvas.md framework
- Define value proposition (value-proposition.md) based on user input
- Document revenue model as described by user
- Document cost structure as described by user

### Step 3: Document Creation
- Write business plan using user-provided information only
- Follow structure defined in Business Plan Structure section
- Fill Tier 1 (MVP-critical) sections with user's input
- Include Tier 2 sections with available information
- Mark unknown items as "TBD - pending review/validation"
- Include user's assumptions as stated (label them as "Assumption:")
- Create document in `projects/[project-name]/01-planning/business-plan.md`

### Step 4: Completion Check
- All user-provided information is captured accurately
- All MUST HAVE information from Step 1 is documented
- Document structure follows defined format
- No assumptions or inferences added beyond user input
- **Task complete** - ready for review phase (separate task)

## Deliverables

Primary:
- `projects/[project-name]/01-planning/business-plan.md`

Supporting:
- `projects/[project-name]/01-planning/market-research.md`
- `projects/[project-name]/01-planning/versions/YYYYMMDD-business-plan-v1.md`

## Completion Conditions

□ All Tier 1 sections complete and detailed
□ Tier 2 sections complete (for standard/complex projects)
□ Tier 3 sections complete or documented as TBD with plan
□ Market research conducted and cited
□ Assumptions explicitly stated and validated
□ Competitive analysis thorough
□ Financial projections realistic
□ Risks identified with mitigation plans
□ Document well-structured and professional

## Common Pitfalls to Avoid

1. **Insufficient market validation** → Always research and cite sources
2. **Vague value proposition** → Be specific about user benefits
3. **Ignoring competition** → Acknowledge and address competitive landscape
4. **Unrealistic projections** → Base on market data and comparable businesses
5. **Missing risk analysis** → Identify risks proactively
6. **Skipping personas** → Define clear target users
7. **No MVP definition** → Clearly define minimum viable scope

## Quality Gates

Before completion:
- [ ] Executive summary compelling and complete
- [ ] Problem-solution fit clearly articulated
- [ ] Target market well-defined with data
- [ ] MVP scope clear and achievable
- [ ] Value proposition differentiated
- [ ] Competitive analysis comprehensive
- [ ] Business model viable
- [ ] KPIs measurable and relevant
- [ ] Risks identified and addressed
- [ ] All sources cited

## Exit Conditions

□ Business plan document exists and is complete
□ All completion conditions satisfied
□ Quality gates passed
□ User approval obtained (STOP POINT in workflow)
□ Ready to proceed to requirements definition
