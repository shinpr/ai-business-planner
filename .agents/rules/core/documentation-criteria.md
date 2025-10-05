# Business Documentation Creation Criteria

## Purpose

Define when and how to create business planning documentation for consistency and quality.

## Core Principle: Always Full Documentation Set

**ALL business planning activities require complete documentation.**

**Rationale**:
- New businesses and products involve **people and money**
- These are **significant decisions** with real consequences
- Every business idea deserves **the same rigorous evaluation**
- Incomplete documentation leads to poor decisions
- Knowledge accumulation requires consistent, complete records

**Therefore**: Regardless of perceived project scale or simplicity, always create the full documentation set.

## Required Documentation for All Projects

Every business planning effort must include:

1. **Session Processing** (if meeting notes/議事録 provided)
2. **Business Plan** (mandatory)
3. **Requirements Definition** (mandatory)
4. **Design Specification** (user decision, but always ask)
5. **Prototype Prompts** (mandatory)
6. **Decision Recording** (mandatory)

**No exceptions.** Even "simple ideas" require full documentation because:
- What seems simple often reveals complexity
- Proper evaluation prevents wasted resources
- Past decisions inform future planning
- Stakeholders need complete context

## Document Definitions

### Business Plan

**Purpose**: Define business opportunity, model, and execution strategy

**When Required**:
- Always (for any new business idea)
- Before prototype generation
- Before requirements definition

**Tier Structure** (from business-plan-creation.md):
- **Tier 1** (Prototype-Critical): MUST HAVE
- **Tier 2** (Business Viability): SHOULD HAVE
- **Tier 3** (Execution Details): COULD HAVE

**Includes**:
- Executive summary
- Problem and solution
- Target market and personas
- MVP definition and core features
- Product core value
- Competitive analysis and differentiation
- Business model
- Go-to-market strategy
- KPIs and success metrics
- Milestones and roadmap
- (Tier 3) Financial projections, operations, team, risks

**Excludes**:
- Detailed product requirements (→ Requirements Document)
- Technical implementation details (→ Prompts)
- Design specifications (→ Design Requirements)

**Quality Gates**:
- All Tier 1 sections complete
- Market research conducted and cited
- Competitive analysis thorough
- Financial projections realistic (if included)
- User approval obtained

### Requirements Document

**Purpose**: Define product/service requirements for MVP

**When Required**:
- After business plan approval
- Before prompt generation
- For all projects (unless extremely simple)

**Includes**:
- Core value definition
- MVP scope
- Feature prioritization (MoSCoW)
- User stories with acceptance criteria
- Functional requirements
- Non-functional requirements
- Technical requirements (high-level)
- Constraints and assumptions
- Validation approach

**Excludes**:
- Business model details (→ Business Plan)
- Detailed design specs (→ Design Requirements)
- Platform-specific prompts (→ Prompts)

**Quality Gates**:
- Core value clearly extracted
- MVP scope minimal but complete
- Features prioritized with MoSCoW
- Requirements traceable to business plan
- User approval obtained

### Design Requirements (Optional)

**Purpose**: Define UI/UX and visual design for prototype

**When Required**:
- When design is critical to MVP
- When brand identity is important
- When user experience needs specification

**When NOT Required**:
- Simple functional prototypes
- Backend-focused products
- When using default AI tool designs

**Includes**:
- Design vision and philosophy
- UI/UX concept
- Visual design (colors, typography, icons)
- Design system elements
- Brand identity (if applicable)
- Accessibility requirements
- Responsive design strategy

**Excludes**:
- Detailed implementation (→ Prompts)
- Business justification (→ Business Plan)

**Quality Gates**:
- Design vision clear
- Specifications sufficient for prompt generation
- User approval obtained

### Prototype Prompts

**Purpose**: Generate AI tool prompts for prototype creation

**When Required**:
- Always (final deliverable before prototype)
- After requirements defined
- After design specified (if applicable)

**Includes**:
- Generic, platform-agnostic prompt
- Platform-specific prompts (Genspark, v0, etc.)
- Context and purpose
- MVP scope and features
- User flows
- Functional specifications
- Design requirements (if applicable)
- Technical preferences
- Success criteria

**Excludes**:
- Business model details (→ Business Plan)
- Market analysis (→ Business Plan)

**Quality Gates**:
- All requirements reflected
- Design elements integrated (if applicable)
- Platform optimizations applied
- Prompts tested for clarity
- User approval obtained

### Session Summary

**Purpose**: Process meeting notes and extract key information

**When Required**:
- When議事録/meeting notes provided
- At start of project (Phase 0)
- After stakeholder meetings

**Includes**:
- Session metadata (date, participants)
- Summary of discussions
- Key decisions extracted
- Action items identified
- Business insights captured
- Requirements extracted
- Risks and issues noted

**Excludes**:
- Detailed business plan (→ Business Plan)
- Full requirements (→ Requirements Document)

**Quality Gates**:
- All decisions extracted
- Action items have owners
- Information organized clearly

### Decision Record

**Purpose**: Document significant business decisions

**When Required**:
- Go/NoGo decisions
- Major strategic choices
- Pivot decisions
- At end of workflow (Phase 5)

**Includes**:
- Decision summary
- Context and background
- Options considered (with pros/cons)
- Decision rationale
- Impact and implications
- Success criteria
- Next steps
- Risks and mitigation

**Excludes**:
- Full business plan (→ Business Plan)
- Implementation details (→ Prompts)

**Quality Gates**:
- Decision clearly stated
- Options analyzed
- Rationale explained
- Risks addressed
- Next steps clear

## Document Relationships

### Creation Flow (Standard Project)
```
Session Notes → Business Plan → Requirements → [Design] → Prompts → Decision
     ↓              ↓              ↓              ↓          ↓          ↓
   Phase 0       Phase 1        Phase 2       Phase 3    Phase 4    Phase 5
```

### Information Flow
- **Business Plan** informs → **Requirements**
- **Requirements** + **Design** inform → **Prompts**
- **All documents** inform → **Decision Record**

### Traceability
- Requirements trace back to Business Plan
- Prompts trace back to Requirements and Design
- Decisions reference all relevant documents

## Storage Structure

| Document | Path | Naming Convention |
|----------|------|------------------|
| Business Plan | `projects/[name]/01-planning/` | `business-plan.md` |
| Requirements | `projects/[name]/02-requirements/` | `requirements.md` |
| Design (optional) | `projects/[name]/03-design/` | `design-requirements.md` |
| Prompts | `projects/[name]/04-prompts/` | `prototype-prompt.md`, `genspark-prompt.md` |
| Sessions | `projects/[name]/05-sessions/` | `YYYYMMDD-[name].md` |
| Decisions | `projects/[name]/06-decisions/` | `YYYYMMDD-[type]-decision.md` |

## Version Control

### Versioning Strategy
- Keep current version at root of category folder
- Store historical versions in `versions/` subfolder
- Use date-based version naming: `YYYYMMDD-[name]-v[N].md`

### When to Create New Version
- Major scope changes
- Pivot decisions
- Significant requirement updates
- After major decision points

## Quality Standards

### All Documents Must Have
□ Clear purpose and scope
□ Complete required sections
□ Consistent formatting
□ Proper markdown structure
□ Citations for external data
□ Date stamps
□ Approval status

### Document-Specific Quality
- **Business Plan**: Market validated, financially viable
- **Requirements**: Traceable, testable, complete
- **Design**: Actionable, consistent, accessible
- **Prompts**: Clear, complete, platform-optimized
- **Decisions**: Rationale clear, risks addressed

## Approval Gates

Each document requires explicit user approval before proceeding:
1. Document created and complete
2. Quality gates passed
3. User reviews
4. User explicitly approves ("yes", "approved", "OK", etc.)
5. Proceed to next phase

## Common Mistakes to Avoid

1. **Skipping business plan** → Always start with business validation
2. **Requirements without business plan** → Ensure business case first
3. **Prompts without requirements** → Define what to build first
4. **No decision documentation** → Record all significant decisions
5. **Version chaos** → Use consistent versioning
6. **Missing traceability** → Link documents clearly
7. **Incomplete quality checks** → Verify all gates passed

## AI Agent Automation Rules

**Always execute full workflow**:
1. Session Processing (if meeting notes provided)
2. Business Plan Creation (Phase 1)
3. Requirements Definition (Phase 2)
4. Design Specification (Phase 3 - always ask user)
5. Prompt Generation (Phase 4)
6. Decision Recording (after Go/NoGo decision)

**No shortcuts or variations**:
- Never skip phases based on perceived simplicity
- Always ask about design specifications (don't assume)
- Always create complete documentation
- Every project uses business-planning-workflow.md

**Quality Standards**:
- Always check for existing documents before creating new
- Maintain traceability across all documents
- Request user approval at each gate
- Review past decisions (projects/*/06-decisions/) in Phase 1
