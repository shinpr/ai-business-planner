# AI Business Planner

**From idea to proposal—create complete business plans through a guided workflow.**

Talk with AI to generate market research, business plans, product requirements (PRD), prototype specs, and pitch decks. Your previous plans help improve the recommendations over time.

## What This Tool Does

1. **Business idea or meeting notes** → AI guides you through a short Q&A to clarify your concept
2. **Business plan** → Market research, competitive analysis, business model design (brings in relevant insights from your previous projects)
3. **PRD** → MVP scope, feature priorities (MoSCoW), user stories
4. **Prototype spec** → Instructions formatted for tools like Genspark or v0
5. **Pitch deck** → Presentation slides (Marp format, exportable to PDF/PowerPoint)
6. **Decision tracking** → Extracts insights from meetings to improve your next plan

## Who This Is For

**Business professionals who use AI tools but aren't technical experts.**

- Business development managers launching new initiatives
- Startup founders and product managers
- Leaders looking to improve their planning process
- Anyone who wants to systematically capture and learn from decisions

## Setup

### What You Need

- **Cursor** (recommended) or **Windsurf**
  - Cursor: https://cursor.sh/ (free plan available)
  - Windsurf: https://codeium.com/windsurf (free)

### Installation

**Option 1: Using Git**

```bash
git clone https://github.com/shinpr/ai-business-planner.git
```

**Option 2: Download ZIP** (if you don't have Git)

Go to https://github.com/shinpr/ai-business-planner, click the green "Code" button, then "Download ZIP". Unzip the file after downloading.

Then open the `ai-business-planner` folder in Cursor or Windsurf.

## How to Use

### Automatic Workflow (Recommended)

In Cursor's Composer or Windsurf, just ask:

```
I want to create a business plan for an online cooking class platform
```

The AI automatically runs through this workflow:

```
Phase 1: Business Plan
  ├── Reference past decisions (after first use)
  ├── Simple guided questions
  ├── Market research (live web data)
  ├── Competitive analysis
  ├── Business model design
  └── Review → Your approval

Phase 2: PRD
  ├── MVP scope definition
  ├── Feature priorities (MoSCoW)
  ├── User stories
  └── Review → Your approval

Phase 3: Design Spec (optional)
  ├── UI/UX concept
  ├── Visual design
  └── Review → Your approval

Phase 4: Prototype Spec
  ├── Generate comprehensive prompt
  ├── Formatted for tools like Genspark/v0
  └── Review → Your approval

Done → Pitch deck (optional)
```

At each phase, you review and approve before moving on.

### Slash Commands (For More Control)

If you want to start at a specific phase or work step by step:

- `/planning-workflow` - Full business planning workflow
- `/business-plan` - Business plan only
- `/define-requirements` - PRD only
- `/generate-prompts` - Prototype spec only
- `/design-spec` - Design spec only
- `/review-document` - Review existing documents
- `/process-session` - Process meeting notes and extract decisions
- `/prepare-proposal` - Create pitch deck

## Key Features

### 1. Turn Meeting Notes Into Business Plans

Got existing notes or transcripts? Turn them into structured plans:

```
Create a business plan from these meeting notes
```

### 2. AI-Powered Plan Review

The AI reviews your business plans for:

- Market information accuracy (checking real web data)
- Competitive analysis completeness
- Business model feasibility
- Improvement suggestions

```
Review this business plan
```

### 3. Prototype Specs Explained

These specs include the essentials needed to build a prototype:

- A clear product summary and target users
- MVP feature list with priorities
- Key user flows
- Design and technical notes (if available)

Hand this to Genspark Developer, v0, or similar tools to build prototypes that align with your business plan.

### 4. Learning From Decisions

A key feature of this tool is that it keeps track of your decisions. Every time you process meeting notes, the AI extracts and records what worked, what failed, which assumptions turned out to be wrong, and which risks actually occurred. When you create your next business plan, these insights are automatically pulled in to provide better guidance. Over time, the recommendations become more tailored to your context.

Share your meeting notes and ask "organize these notes" to have AI extract and record decisions.

### 5. Pitch Deck Generation

Auto-generate presentations from your business plan, PRD, and prototype spec. The output is in Marp format—a simple markdown-based tool that lets you export to PDF, PowerPoint, or HTML.

```
Create a pitch deck
```

## Where Files Are Saved

All files are saved automatically in a clear folder structure. You don't need to manage files manually.

```
projects/your-project/
├── 01-planning/         # Business plans, market research
├── 02-requirements/     # PRD
├── 03-design/          # Design specs (if created)
├── 04-prompts/         # Prototype specs
├── 05-sessions/        # Meeting notes
├── 06-decisions/       # Decision records (auto-used in future plans)
└── 07-artifacts/       # Pitch decks and other outputs
```

## Built-in Business Frameworks

The tool automatically applies proven methodologies:

- **Business Model Canvas**: A one-page template to map out how your business creates and delivers value
- **Value Proposition Canvas**: Helps you match what you're offering to what customers actually need
- **Market Analysis**: Estimates your market size (total, serviceable, and realistic target), analyzes competitors, and builds customer personas
- **MVP Definition**: Uses lean startup thinking to identify the smallest version of your product worth building, with MoSCoW method—a way to rank features by Must have, Should have, Could have, and Won't have
- **Prompt Engineering**: Writing clear instructions for AI tools so they produce the results you want
- **Design Thinking**: A human-centered approach to designing products that starts with understanding user needs

## Customizing the Output Language

By default, the AI responds in whatever language you use. If you want to guarantee all outputs are in a specific language, you can add a rule to `AGENTS.md`.

**How to do it:**

1. Open `AGENTS.md` in the project folder
2. Find the section called `## Core Principles`
3. Add the following text right after `## Core Principles` (before `### Plan Injection`):

```markdown
### Language Strategy [MANDATORY]
**User-facing content in Japanese:**
- **User interaction** (conversation, responses, questions): Communicate in Japanese
- **Deliverables** (business plans, requirements, prompts, documentation): Write in Japanese
```

**For other languages:** Replace "Japanese" with your language. For example, if you want Spanish output:

```markdown
### Language Strategy [MANDATORY]
**User-facing content in Spanish:**
- **User interaction** (conversation, responses, questions): Communicate in Spanish
- **Deliverables** (business plans, requirements, prompts, documentation): Write in Spanish
```

## FAQ

**Q: Which tools work with this?**
A: Cursor (recommended), Windsurf, and other tools that support the [AGENTS.md standard](https://agents.md) (Aider, Zed, etc.).

**Q: How accurate are the generated plans?**
A: The AI does market research and validation, but always apply your own judgment. That said, plans improve over time as your decision history builds up.

**Q: Can I customize it?**
A: Yes. Edit files in `.agents/` to add your own frameworks or templates.

**Q: Is it free?**
A: The framework is free (MIT License). AI tools like Cursor may have their own costs.

## License

MIT License - free to use, including commercially.

---

**Build better business plans by learning from every decision.**

Built on [AGENTS.md](https://agents.md) and works with multiple AI development tools.

```bash
git clone https://github.com/shinpr/ai-business-planner.git
```
