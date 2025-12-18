# Design Specification

## Required Rules [MANDATORY - MUST BE ACTIVE]

**RULE AVAILABILITY VERIFICATION:**
1. [LOAD] `.agents/rules/business/design-thinking.md`
2. [LOAD] `.agents/rules/core/documentation-criteria.md`
3. [VERIFY ACTIVE] `.agents/rules/core/metacognition.md` (from session start)

## Purpose

Define design requirements and specifications for prototype, including UI/UX concept, visual design, and brand elements.

## Entry Conditions

□ Requirements document exists and approved
□ Product core value understood
□ Target users and personas defined
□ All required rules loaded and active

## Design Specification Structure

### 1. Design Vision
- Overall design philosophy
- User experience goals
- Brand personality
- Design principles

### 2. UI/UX Concept
- Interface concept
- Interaction patterns
- User flow considerations
- Usability goals

### 2.5 Atmosphere Translation

Translate abstract brand/industry attributes into concrete design elements.

**Required outputs:**
- 3-5 atmosphere keywords from business plan
- Design direction for: colors, border-radius, shadows, spacing, typography
- Reference materials (URLs, images) if available
- Elements to avoid

### 3. Visual Design
- Color palette
- Typography
- Iconography
- Imagery style

### 4. Design System Elements
- Component library needs
- Spacing and layout
- Grid system
- Responsive breakpoints

### 5. Brand Identity (if applicable)
- Logo usage
- Brand colors
- Brand voice
- Brand guidelines

### 6. Accessibility Requirements
- WCAG compliance level
- Screen reader support
- Keyboard navigation
- Color contrast requirements

### 7. Responsive Design
- Mobile-first approach
- Breakpoint definitions
- Adaptive vs responsive
- Device support

## Execution Process

### Step 0: Interactive Information Gathering [IF NEEDED]

**Context**: This task usually follows requirements definition. Most information comes from requirements and business plan. However, users may have specific design preferences or constraints.

**NO ASSUMPTIONS ALLOWED**: Never infer, guess, or assume design preferences not explicitly provided by the user or documented in previous phases.

**Process**:
1. **Extract existing information** from:
   - Requirements document (primary source)
   - Business plan (brand/target audience)
   - User input and discussions
   - Provided design materials (if any)

2. **Identify gaps** in design-specific information (see checklist below)

3. **Interactive dialogue with user** (if gaps exist):
   - Ask specific questions for missing design information
   - Group questions by category (visual, UX, accessibility, etc.)
   - Wait for user response before proceeding
   - **NEVER fill gaps with assumptions**

4. **Skip this step if**:
   - Requirements contain sufficient design direction
   - No specific design preferences needed

**Required Information Checklist** (ask only if missing from previous documents):

**Design Vision** (SHOULD HAVE):
- [ ] Design philosophy or style preference (modern, minimal, bold, etc.)?
- [ ] Brand personality (if not in business plan)
- [ ] Design references or inspiration (if any)?
- [ ] Specific design constraints or preferences?

**Atmosphere** (SHOULD HAVE):
- [ ] Atmosphere keywords (3-5 adjectives describing brand/industry feel)
- [ ] Design references or inspiration
- [ ] Elements to avoid

**Visual Elements** (SHOULD HAVE):
- [ ] Color preferences or brand colors?
- [ ] Typography preferences?
- [ ] Existing brand guidelines to follow?

**User Experience** (MUST HAVE):
- [ ] Primary device target (mobile-first, desktop-first)?
- [ ] Critical user flows that need special attention?
- [ ] Accessibility requirements (WCAG level, etc.)?

**Constraints** (IF APPLICABLE):
- [ ] Technical limitations affecting design?
- [ ] Platform-specific design requirements?

**PROCEED CONDITION**: All MUST HAVE items confirmed or marked as "TBD - designer's discretion based on best practices"

### Step 1: Understand User Needs
- Review requirements and personas
- Identify user experience priorities
- Understand user context
- Define usability goals

### Step 2: Define Design Vision
- Establish design philosophy
- Set experience goals
- Define brand personality
- Create design principles

### Step 3: Create UI/UX Concept
- Sketch interface concepts
- Define interaction patterns
- Design user flows
- Prioritize usability

### Step 4: Specify Visual Design
- Choose color palette
- Select typography
- Define iconography
- Establish visual style

### Step 5: Document Design System
- List component needs
- Define spacing/layout
- Set grid system
- Specify responsive approach

### Step 6: Address Accessibility
- Set accessibility goals
- Define compliance level
- Plan inclusive design
- Test considerations

## Deliverables

Primary:
- `projects/[project-name]/03-design/design-requirements.md`
- `projects/[project-name]/03-design/ui-concept.md`

Supporting:
- `projects/[project-name]/03-design/assets/` (mockups, color palettes, etc.)

## Design Requirements Template

```markdown
# Design Requirements: [Product Name]

## Design Vision
[Overall design philosophy and goals]

## UI/UX Concept
- **Interface Style**: [Description]
- **Interaction Patterns**: [Key interactions]
- **User Flows**: [Primary flows]
- **Usability Goals**: [Goals]

## Visual Design
### Color Palette
- Primary: [Color + Hex]
- Secondary: [Color + Hex]
- Accent: [Color + Hex]
- Neutral: [Grays]

### Typography
- Headings: [Font family, sizes]
- Body: [Font family, sizes]
- UI Text: [Font family, sizes]

### Iconography
- Icon style: [Description]
- Icon set: [If using library]

## Design System
- **Components**: [List needed]
- **Spacing**: [Scale e.g., 4px, 8px, 16px]
- **Grid**: [Column count, gutters]
- **Breakpoints**: [Mobile, Tablet, Desktop]

## Brand Identity
- **Logo**: [Usage guidelines]
- **Colors**: [Brand colors]
- **Voice**: [Tone and style]

## Accessibility
- **WCAG Level**: [A/AA/AAA]
- **Features**: [Required features]

## Responsive Design
- **Approach**: [Mobile-first/Desktop-first]
- **Breakpoints**: [Specific breakpoints]
- **Device Support**: [List]
```

## Completion Conditions

□ Design vision clearly articulated
□ UI/UX concept defined
□ Visual design specified
□ Design system documented
□ Brand elements included (if applicable)
□ Accessibility requirements set
□ Responsive approach defined
□ Design supports requirements
□ Design deliverable for prompt generation

## Common Pitfalls to Avoid

1. **Over-designing for MVP** → Keep it simple and focused
2. **Ignoring accessibility** → Plan for inclusive design
3. **No responsive strategy** → Always consider multiple devices
4. **Inconsistent design system** → Define clear patterns
5. **Missing user context** → Design for actual user needs
6. **No brand consideration** → Include basic brand elements
7. **Vague specifications** → Be specific and actionable

## Exit Conditions

□ Design requirements document exists
□ All completion conditions satisfied
□ User approval obtained (STOP POINT in workflow)
□ Design ready to integrate into prompts
