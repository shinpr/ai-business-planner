# Document Review

## Required Rules [MANDATORY - MUST BE ACTIVE]

**RULE AVAILABILITY VERIFICATION:**
1. [LOAD] `.agents/rules/core/documentation-criteria.md`
2. [VERIFY ACTIVE] `.agents/rules/core/metacognition.md` (from session start)
3. [LOAD IF APPLICABLE] Business-specific rules based on document type:
   - Business Plan → business-model-canvas.md, value-proposition.md, market-analysis.md
   - Requirements → mvp-definition.md
   - Design → design-thinking.md
   - Prompts → prompt-engineering.md

## Purpose

Review and validate business planning documents (business plans, requirements, design specs, prompts) for quality, completeness, accuracy, and market viability. Provide actionable feedback and facilitate improvements through user collaboration.

## Entry Conditions

□ Document exists and path is provided
□ Document type is identified (business-plan, requirements, design, prompts)
□ Required rules for document type are loaded
□ Review criteria understood

## Document Types Supported

1. **Business Plan** (`projects/[name]/01-planning/business-plan.md`)
2. **Requirements** (`projects/[name]/02-requirements/requirements.md`)
3. **Design Specification** (`projects/[name]/03-design/design-requirements.md`)
4. **Prototype Prompts** (`projects/[name]/04-prompts/*.md`)

## Review Execution Process

### Step 1: Document Analysis

1. **Read the document** completely
2. **Identify document type** automatically from path and content
3. **Load type-specific rules** if not already active
4. **Extract key elements**:
   - Core claims and assumptions
   - Market data and citations
   - Business logic and rationale
   - Completeness of required sections

### Step 2: Quality Assessment

**For Business Plans**:
- [ ] All Tier 1 (MVP-critical) sections complete and detailed
- [ ] Problem-solution fit clearly articulated
- [ ] Target market well-defined with data or explicit assumptions
- [ ] Value proposition differentiated and compelling
- [ ] Competitive landscape acknowledged
- [ ] Business model viable and realistic
- [ ] Assumptions explicitly stated and labeled
- [ ] Risks identified with mitigation approaches
- [ ] Financial projections reasonable (or marked as assumptions)
- [ ] All sections follow business-model-canvas.md framework

**For Requirements**:
- [ ] Core value clearly defined and traceable to business plan
- [ ] MVP scope well-defined using MoSCoW
- [ ] User stories complete with acceptance criteria
- [ ] Functional requirements clear and specific
- [ ] Non-functional requirements addressed
- [ ] Success criteria measurable
- [ ] Traceability to business plan maintained

**For Design Specifications**:
- [ ] Design vision aligned with product requirements
- [ ] User experience priorities clear
- [ ] Visual design elements specified
- [ ] Accessibility requirements defined
- [ ] Responsive design approach documented
- [ ] Component system outlined
- [ ] Design rationale provided

**For Prototype Prompts**:
- [ ] All requirements from requirements doc included
- [ ] Platform-specific optimizations applied
- [ ] Technical stack specified
- [ ] Success criteria clear
- [ ] Design elements incorporated (if applicable)
- [ ] Prompt is actionable and complete

### Step 3: Market Research & Validation [FOR BUSINESS PLANS]

**Only for business plans** - validate assumptions with research:

1. **Identify validation needs**:
   - Market size claims
   - Competitive landscape assumptions
   - Industry trends mentioned
   - Technology adoption rates
   - User behavior assumptions

2. **Conduct research** (search the web using SESSION_BASELINE_DATE):
   - Validate market data
   - Research competitors
   - Verify industry trends
   - Gather supporting evidence
   - Identify contradicting data

3. **Document findings**:
   - Validations (assumptions confirmed)
   - Concerns (assumptions challenged)
   - Gaps (missing critical information)
   - Opportunities (additional insights)

### Step 4: Findings Presentation to User

**Structure feedback clearly**:

```markdown
# Document Review Results

## Document: [document name and type]

## Overall Assessment
[Summary: Strong points and main concerns]

## ✅ Strengths
1. [Strength 1]
2. [Strength 2]
...

## ⚠️ Issues Found

### Critical (Must Fix)
1. **[Issue title]**
   - Current state: [what's wrong]
   - Impact: [why it matters]
   - Recommendation: [how to fix]

### Important (Should Fix)
1. **[Issue title]**
   - Current state: [what's wrong]
   - Impact: [why it matters]
   - Recommendation: [how to fix]

### Minor (Nice to Fix)
1. **[Issue title]**
   - Current state: [what's wrong]
   - Recommendation: [how to fix]

## 🔍 Research Findings [Business Plans Only]

### Validated Assumptions ✓
- [Assumption 1]: [Research supports this]
- [Assumption 2]: [Data confirms this]

### Challenged Assumptions ⚠️
- [Assumption 1]: [Research suggests otherwise]
- [Evidence]: [Source and data]

### Additional Insights
- [Insight 1]: [Opportunity or consideration]
- [Insight 2]: [Market trend or data point]

## 📋 Recommended Actions
1. [Action 1 - priority level]
2. [Action 2 - priority level]
...

## Next Steps
[What user should decide or do next]
```

**STOP POINT**: Present findings and WAIT for user response. Do not proceed without user input.

### Step 5: Interactive Improvement

**User may respond with**:
1. **Accept recommendations**: "Fix the critical issues"
2. **Partial acceptance**: "Fix issues 1 and 3, but skip 2"
3. **Questions/Discussion**: "Why is X an issue?"
4. **Reject**: "I disagree with Y"
5. **Request changes**: "Also add Z to the document"

**Your response**:
1. **For questions**: Explain reasoning, provide examples, discuss alternatives
2. **For acceptance**: Confirm which changes to make, then proceed to Step 6
3. **For rejection**: Understand user's perspective, document as conscious decision
4. **For requests**: Clarify requirements, then incorporate in Step 6

**Multiple rounds OK**: Continue discussion until user approves a change plan

### Step 6: Document Update [ONLY AFTER USER APPROVAL]

1. **Create backup** (if first review):
   ```bash
   cp projects/[name]/[phase]/[doc].md projects/[name]/[phase]/versions/$(date +%Y%m%d)-[doc]-pre-review.md
   ```

2. **Apply approved changes**:
   - Fix critical issues (must)
   - Fix important issues (should, if approved)
   - Fix minor issues (if approved)
   - Incorporate research findings (if approved)
   - Add any user-requested additions

3. **Maintain document integrity**:
   - Preserve user's original voice and intent
   - Keep user-provided information accurate
   - Mark new assumptions clearly as "Assumption (from research):"
   - Add citations for research-based additions

4. **Save updated document**

5. **Create version** (if significant changes):
   ```bash
   cp projects/[name]/[phase]/[doc].md projects/[name]/[phase]/versions/$(date +%Y%m%d)-[doc]-reviewed-v2.md
   ```

### Step 7: Review Completion

1. **Summarize changes made**:
   - List all modifications
   - Highlight key improvements
   - Note any remaining TBD items

2. **Confirm completion** with user:
   - "Review complete. Document updated with approved changes."
   - "Remaining items marked as TBD: [list if any]"
   - "Ready to proceed to next phase? (Y/N)"

3. **Exit if user approves**, or return to Step 5 for further iterations

## Deliverables

Primary:
- Updated document at original location (with approved improvements)

Supporting:
- `projects/[project-name]/[phase]/versions/YYYYMMDD-[doc]-pre-review.md` (backup before review)
- `projects/[project-name]/[phase]/versions/YYYYMMDD-[doc]-reviewed-v[N].md` (if significant changes)

## Completion Conditions

□ Document thoroughly reviewed against quality criteria
□ All issues identified and categorized (critical/important/minor)
□ Research conducted and findings presented (for business plans)
□ User feedback received and discussed
□ Approved changes implemented
□ Document updated and versioned
□ User confirms review completion

## Common Review Patterns

### Business Plan Reviews
- Validate market size with research
- Challenge assumptions with data
- Ensure competitive analysis is realistic
- Verify financial projections are grounded
- Check persona definitions are specific

### Requirements Reviews
- Ensure traceability to business plan
- Verify MVP scope is truly minimal
- Check user stories are testable
- Validate success criteria are measurable
- Ensure non-functional requirements considered

### Design Reviews
- Align design vision with user needs
- Verify accessibility standards
- Check responsive design approach
- Ensure brand consistency
- Validate usability priorities

### Prompt Reviews
- Verify all requirements included
- Check platform-specific optimizations
- Ensure technical stack is clear
- Validate prompt completeness
- Test prompt actionability

## Quality Gates

Before completion:
- [ ] All document sections reviewed
- [ ] Quality criteria assessed
- [ ] Research conducted (if applicable)
- [ ] Findings presented to user clearly
- [ ] User feedback incorporated
- [ ] Changes approved by user
- [ ] Document updated correctly
- [ ] Versions created

## Exit Conditions

□ Review process completed
□ All approved changes implemented
□ User satisfied with document quality
□ Ready for next phase or iteration
