# Prototypes prompts workflow

A structured workflow for AI-assisted prototyping with user testing and markdown plan tracking.

## Core principle

**A working prototype in hand is more valuable than written specs.**

Every feature specification must link to its working prototype. Engineers should interact with the prototype before reading requirements. The prototype demonstrates behaviour; the spec documents edge cases and implementation notes.

## Quick reference

| Step | Prompt file | When to use |
|------|-------------|-------------|
| 1 | head-of-design.md | Start of any prototype work |
| 2 | explore.md | Understand the problem, research patterns, select components |
| 3 | create-plan.md | Generate markdown execution plan with progress tracking |
| 4 | execute.md | Build the prototype, task by task |
| 5 | review.md | Code and UI/UX review after implementation |
| 6 | peer-review.md | Cross-check with another model (optional) |
| 7 | design-test.md | Create test plan, questions, and success metrics |
| 8 | analyse-feedback.md | Analyse results and recommend improvements |
| 9 | document.md | Update docs and changelog |

**Standalone prompts:**
- create-issue.md: Capture bugs/features mid-development or during iterations
- learning-opportunity.md: Understand design decisions with defensible rationale

## Setup

Before using, update `head-of-design.md` with your component library, design system, and research tools.
