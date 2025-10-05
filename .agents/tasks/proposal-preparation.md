# Proposal Preparation

## Required Rules [MANDATORY - MUST BE ACTIVE]

**RULE AVAILABILITY VERIFICATION:**
1. [LOAD] `.agents/rules/core/documentation-criteria.md`
2. [VERIFY ACTIVE] `.agents/rules/core/metacognition.md` (from session start)

## Purpose

Prepare presentation materials (Marp-compatible slide deck) for stakeholder presentations. This is an **independent task**, not part of the core workflow.

**Note**: Go/NoGo decisions are recorded through session-processing.md (during meetings) and decision-recording.md (formal documentation).

## When to Use This Task

- Creating pitch deck for investors
- Preparing presentation for management
- Building stakeholder proposal
- Creating demo day materials

## Entry Conditions

□ Business plan complete
□ Requirements defined
□ Prompts generated (optional but recommended)
□ Design specifications complete (if applicable)
□ All required rules loaded and active

## Presentation Format

This task generates **Marp-compatible markdown** for creating professional slide decks.

### About Marp

Marp (Markdown Presentation Ecosystem) converts markdown to slides:
- **Export formats**: PDF, PPTX, HTML
- **Tools**: VS Code extension, CLI, web app
- **Syntax**: Simple markdown with `---` for slide breaks
- **Website**: https://marp.app

## Slide Deck Structure

### Standard Business Proposal Deck (12-15 slides)

```markdown
---
marp: true
theme: default
paginate: true
---

# Slide 1: Title
# Slide 2: Problem
# Slide 3: Solution
# Slide 4: Market Opportunity
# Slide 5: Product/MVP
# Slide 6: Business Model
# Slide 7: Competitive Advantage
# Slide 8: Go-to-Market Strategy
# Slide 9: Financial Projections
# Slide 10: Team (if applicable)
# Slide 11: Milestones & Roadmap
# Slide 12: Ask/Next Steps
```

## Execution Process

### Step 1: Gather All Materials
- Read business plan document
- Read requirements document
- Read prompt documents (if generated)
- Read design specifications (if applicable)
- Identify key messages

### Step 2: Synthesize Key Points
- Extract most compelling data
- Identify strongest value propositions
- Select key competitive advantages
- Choose critical metrics
- Highlight validation/traction

### Step 3: Create Marp Markdown
- Write title slide
- Build problem narrative
- Present solution clearly
- Show market opportunity with data
- Demonstrate product/MVP
- Explain business model
- Highlight competitive positioning
- Present go-to-market strategy
- Show financial projections
- Include team (if applicable)
- Show milestones and roadmap
- Close with clear ask/next steps

### Step 4: Visual Enhancement
- Use bullet points effectively (3-5 per slide)
- Include data/charts where possible (describe for manual creation)
- Add images/mockups (placeholder references)
- Use consistent formatting
- Apply visual hierarchy

### Step 5: Quality Check
- One key message per slide
- No text overload
- Clear narrative flow
- Data properly cited
- Compelling story

## Deliverables

Primary:
- `projects/[project-name]/07-artifacts/presentations/proposal-slides.md` (Marp format)

Supporting:
- `projects/[project-name]/07-artifacts/presentations/speaker-notes.md` (optional)
- `projects/[project-name]/07-artifacts/presentations/versions/` (version history)

## Marp Slide Template

```markdown
---
marp: true
theme: default
paginate: true
style: |
  section {
    background-color: #fff;
  }
  h1 {
    color: #2c3e50;
  }
---

<!-- Slide 1: Title -->
# [Product Name]
## [Tagline/Value Proposition]

**Presenter**: [Name]
**Date**: [YYYY-MM-DD]

---

<!-- Slide 2: Problem -->
# The Problem

- **Pain Point 1**: [Description with data]
- **Pain Point 2**: [Description with data]
- **Pain Point 3**: [Description with data]

> "Quote from target customer highlighting problem"

---

<!-- Slide 3: Solution -->
# Our Solution

**[Product Name]** solves this by:

- ✅ [Key benefit 1]
- ✅ [Key benefit 2]
- ✅ [Key benefit 3]

---

<!-- Slide 4: Market Opportunity -->
# Market Opportunity

- **TAM** (Total Addressable Market): $[X]B
- **SAM** (Serviceable Addressable Market): $[Y]M
- **SOM** (Serviceable Obtainable Market): $[Z]M

**Market Growth**: [X]% CAGR

---

<!-- Slide 5: Product/MVP -->
# Product Overview

## Core Features (MVP)
1. **[Feature 1]**: [Brief description]
2. **[Feature 2]**: [Brief description]
3. **[Feature 3]**: [Brief description]

[Add mockup/screenshot image here]

---

<!-- Slide 6: Business Model -->
# Business Model

**Revenue Streams**:
- [Revenue stream 1]: [Pricing]
- [Revenue stream 2]: [Pricing]

**Target Customers**: [Segment]

**Customer Acquisition**: [Primary channel]

---

<!-- Slide 7: Competitive Advantage -->
# Why We'll Win

| Competitor | Us |
|------------|-----|
| [Weakness 1] | [Our strength 1] |
| [Weakness 2] | [Our strength 2] |
| [Weakness 3] | [Our strength 3] |

**Unique Advantage**: [Key differentiator]

---

<!-- Slide 8: Go-to-Market Strategy -->
# Go-to-Market Strategy

**Phase 1** (Months 1-3):
- [Action 1]
- [Action 2]

**Phase 2** (Months 4-6):
- [Action 3]
- [Action 4]

**Key Metrics**: [Metric 1], [Metric 2]

---

<!-- Slide 9: Financial Projections -->
# Financial Projections

| Year | Revenue | Customers | ARR |
|------|---------|-----------|-----|
| Y1   | $[X]K   | [N]       | $[Y]K |
| Y2   | $[X]M   | [N]K      | $[Y]M |
| Y3   | $[X]M   | [N]K      | $[Y]M |

**Break-even**: Month [N]

---

<!-- Slide 10: Team (Optional) -->
# Team

**[Founder Name]** - CEO
- [Key experience/achievement]

**[Team Member 2]** - [Role]
- [Key experience/achievement]

**Advisors**: [Notable advisor names]

---

<!-- Slide 11: Milestones & Roadmap -->
# Milestones & Roadmap

**Q1 2025**
- ✅ [Completed milestone]
- 🔄 [In progress milestone]

**Q2 2025**
- [ ] [Planned milestone]
- [ ] [Planned milestone]

**Q3-Q4 2025**
- [ ] [Future milestone]

---

<!-- Slide 12: Ask/Next Steps -->
# Next Steps

## The Ask
[What you're requesting - funding, approval, partnership, etc.]

## Next Steps
1. [Action 1]
2. [Action 2]
3. [Action 3]

**Contact**: [Email/Website]

---

<!-- Backup Slides -->
# Appendix

Additional details available on request:
- Detailed financial model
- Full market research
- Technical architecture
- Customer testimonials

```

## Presentation Tips

### Content Guidelines
- **One idea per slide**: Keep focus clear
- **Visual hierarchy**: Use size and color for emphasis
- **Data-driven**: Include numbers and evidence
- **Storytelling**: Create narrative arc
- **Call to action**: Clear ask and next steps

### Marp-Specific Tips
- Use `---` to separate slides
- Use `<!--` comments `-->` for slide titles/notes
- Apply custom CSS in frontmatter `style:` section
- Use `![bg](image.jpg)` for background images
- Use `![width:500px](image.jpg)` for sized images

### Common Mistakes to Avoid
- Too much text per slide
- Inconsistent formatting
- Missing data/sources
- Weak problem definition
- Unclear ask
- No visual interest

## Completion Conditions

□ Slide deck created in Marp format
□ All key messages included
□ Story flows logically
□ Data properly cited
□ Visual hierarchy clear
□ Compelling and professional
□ Ready to convert to PDF/PPTX via Marp

## Export Instructions for User

After reviewing the markdown:

1. **Using Marp CLI**:
   ```bash
   marp proposal-slides.md -o proposal-slides.pdf
   marp proposal-slides.md -o proposal-slides.pptx
   ```

2. **Using VS Code**:
   - Install "Marp for VS Code" extension
   - Open proposal-slides.md
   - Click "Export slide deck" button
   - Choose format (PDF/PPTX/HTML)

3. **Using Marp Web**:
   - Visit https://web.marp.app
   - Paste markdown content
   - Export to desired format

## Exit Conditions

□ Marp-compatible markdown created
□ All completion conditions satisfied
□ File saved in presentations directory
□ User can export to presentation format
□ Ready for stakeholder presentation
