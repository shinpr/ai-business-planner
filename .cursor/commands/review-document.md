# Document Review

Execute document review task. Follow the task definition strictly.

`.agents/tasks/document-review.md`

**Instructions:**
- If the user has specified a document path, review that document
- If the user has NOT specified a document path, ask the user which document they want to review
- Supported document types: business plans, requirements, design specs, prompts
- Follow the review process defined in the task file: analyze, assess quality, conduct research (if applicable), present findings, wait for user approval, then update document
