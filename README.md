# AI Business Planner

Turn an idea or meeting notes into a business plan that shows what is known, what is assumed, and what to validate next.

AI Business Planner is a set of instructions for AI agents such as Cursor. It helps non-technical business users create decision-useful plans, MVP requirements, prototype-generation prompts, and proposals while keeping the documents connected.

It can run one task at a time or guide an end-to-end workflow. Each request creates the selected output; the end-to-end sequence runs when you request it.

## See the Output First

The [AI Business Planner Demo](https://github.com/shinpr/ai-business-planner-demo) shows an example from business plan through prototype prompt and pitch deck.

Use it to see:

- how assumptions and missing evidence are represented;
- how an MVP scope traces back to the business idea;
- how the requirements become a prototype-generation prompt;
- how the same source material supports a proposal.

## First Run

### 1. Install an AI editor

[Cursor](https://cursor.com/download) is the recommended option because this repository includes Cursor slash commands. Other agents that read [`AGENTS.md`](https://agents.md/) can use the natural-language tasks.

### 2. Download this repository

If you use Git:

```bash
git clone https://github.com/shinpr/ai-business-planner.git
```

If you do not use Git:

1. Open the [repository page](https://github.com/shinpr/ai-business-planner).
2. Select **Code → Download ZIP**.
3. Extract the downloaded ZIP file.

### 3. Open the folder

Open the `ai-business-planner` folder in Cursor, then open Agent chat.

### 4. Describe the result you need

For example:

```text
I want to evaluate an online cooking class business.
Create a business plan, distinguish evidence from assumptions, and show me what to validate next.
```

You can write in your preferred language. To keep the conversation and saved documents in one language, state it in the same request:

```text
日本語で対話し、成果物も日本語で保存してください。
```

The agent reads the repository instructions, uses information already provided before asking questions, researches current claims when needed, and saves the requested document under `projects/`.

## Common Starting Points

### Start from meeting notes

```text
Create a reusable session summary from these meeting notes. Separate decisions, actions, insights, and open questions.
```

### Review an existing plan

```text
Review projects/my-project/01-planning/business-plan.md for the decision it needs to support. Show findings before changing the file.
```

### Define an MVP

```text
Use the approved business plan in projects/my-project/01-planning/ to define the smallest MVP that can test its core hypothesis.
```

### Create a prototype prompt

```text
Create a v0 prompt from the requirements in projects/my-project/02-requirements/. Match the implementation fidelity to the validation goal.
```

### Run the complete workflow

```text
Take this idea from business validation through an MVP definition and a prototype-generation prompt. Pause for my agreement when the business direction and MVP scope are ready.
```

The complete workflow is:

```text
Business direction
    ↓ agreement
MVP requirements
    ↓ agreement
Design direction, when it affects the prototype
    ↓
Prototype-generation prompt
```

Proposal preparation, formal decision records, and meeting summaries remain available when you request them.

## Cursor Slash Commands

Cursor users can start a task directly:

| Command | Result |
|---|---|
| `/planning-workflow` | Business idea through prototype prompt |
| `/business-plan` | Business plan and validation priorities |
| `/define-requirements` | MVP requirements |
| `/design-spec` | Design requirements |
| `/generate-prompts` | Prototype-generation prompt |
| `/review-document` | Review of an existing document |
| `/process-session` | Meeting or transcript summary |
| `/prepare-proposal` | Marp-compatible proposal deck |

These commands are adapters to the same task definitions used by natural-language requests.

## Where Documents Are Saved

```text
projects/your-project/
├── 01-planning/       # Business plans and reusable market research
├── 02-requirements/   # MVP requirements
├── 03-design/         # Design requirements when needed
├── 04-prompts/        # Prototype prompts and requested guides
├── 05-sessions/       # Meeting and session records
├── 06-decisions/      # Significant decision records
└── 07-artifacts/      # Proposals and other outputs
```

Git history is the default document history. Projects can keep separate dated versions when a handoff requires them.

## How the Planning Approach Works

The repository uses familiar business methods where they help a real decision:

- Business Model Canvas for model dependencies and trade-offs;
- Value Proposition Canvas for customer evidence and value hypotheses;
- market analysis for current external evidence;
- MoSCoW or RICE when prioritization needs a reviewable method;
- design thinking when user or experience evidence affects the prototype;
- decision frameworks matched to impact and reversibility.

The sequence is:

```text
Hypothesis → Smallest credible test → Evidence → Decision
```

Framework sections, research, documents, and follow-up work are included according to the requested outcome. Assumptions and unknowns remain visible so a polished document is not mistaken for validated evidence.

## Scope and Limits

This repository provides agent instructions and document conventions. The selected AI editor or agent performs the file operations and web research, subject to its model, tools, permissions, and network access.

Review important business, legal, financial, market, and regulatory claims before acting on them. Generated plans organize evidence and decisions; they do not replace accountable professional judgment.

## Customization

- Edit `AGENTS.md` to change project-wide behavior.
- Edit `.agents/tasks/` to change a task's process or output.
- Edit `.agents/rules/` to change the business criteria used by tasks.
- Edit `.cursor/commands/` to change Cursor slash-command adapters.

Keep project-specific evidence and decisions under `projects/` rather than turning one project's preference into a global rule.

## License

[MIT License](LICENSE) — free to use, modify, and distribute, including commercially.
