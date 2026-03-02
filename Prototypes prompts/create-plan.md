# Plan creation stage

Based on our full exchange, produce a markdown plan document.

## Requirements for the plan

- Include clear, minimal, concise steps.
- Track the status of each step using these emojis:
  - 🟩 Done
  - 🟨 In Progress
  - 🟥 To Do
- Include dynamic tracking of overall progress percentage (at top).
- Do NOT add extra scope or unnecessary complexity beyond explicitly clarified details.
- Steps should be modular, minimal, and use existing components where possible.

## Markdown template

<output_template>
# Prototype Implementation Plan

**Overall Progress:** `0%`

## TLDR
Short summary of what we're prototyping and the hypothesis we're testing.

## Test hypothesis
What we're trying to validate with this prototype.

## Design decisions
Key UI/UX choices made during exploration:
- Decision 1: [choice] - [brief rationale]
- Decision 2: [choice] - [brief rationale]

## Component selections
Components from @moha/component-library:
- [Component name] - [usage in prototype]
- [Component name] - [usage in prototype]

Custom implementations needed:
- [Description] - [why not in library]

## Success metrics preview
How we'll measure if the prototype succeeds:
- Metric 1: [description] - [target]
- Metric 2: [description] - [target]

## Tasks

- [ ] 🟥 **Step 1: [Name]**
  - [ ] 🟥 Subtask 1
  - [ ] 🟥 Subtask 2

- [ ] 🟥 **Step 2: [Name]**
  - [ ] 🟥 Subtask 1
  - [ ] 🟥 Subtask 2

...
</output_template>

Again, it's still not time to build yet. Write the clear plan document. No extra complexity or extra scope beyond what we discussed.

---

## After user approves the plan

Confirm: "Plan ready. Use this markdown file to track progress as you work through each step."
