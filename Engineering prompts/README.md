# Engineering prompts workflow

A structured workflow for AI-assisted development with markdown plan tracking.

## Quick reference

| Step | Prompt file | When to use |
|------|-------------|-------------|
| 1 | cto.md | Start of any feature/bug work |
| 2 | explore.md | Understand the problem before coding |
| 3 | create-plan.md | Generate markdown execution plan with progress tracking |
| 4 | execute.md | Build the feature, task by task |
| 5 | review.md | Code review after implementation |
| 6 | peer-review.md | Cross-check with another model |
| 7 | document.md | Update docs and changelog |

**Standalone prompts:**
- create-issue.md: Capture bugs/features mid-development
- learning-opportunity.md: Shift to teaching mode when stuck

## Full workflow

### 1. Start a feature or bug fix

Run **cto.md**.

The CTO role asks clarifying questions until the scope is clear. Breaks work into phases. Pushes back on unclear requirements.

### 2. Explore the codebase

Run **explore.md**.

Investigates the existing code. Identifies dependencies, edge cases, and constraints. Surfaces ambiguities before any code is written.

### 3. Create the execution plan

Run **create-plan.md**.

Produces a markdown plan with:
- TLDR
- Critical decisions
- Tasks with status tracking (🟩🟨🟥)
- Overall progress percentage

### 4. Execute the plan

Run **execute.md**.

The prompt:
1. Works through tasks from the markdown plan
2. Updates status emojis as tasks progress (🟥 → 🟨 → 🟩)
3. Updates overall progress percentage
4. Notes any deviations or decisions

### 5. Review the code

Run **review.md**.

Checks for:
- Logging and error handling
- TypeScript types
- Security issues
- Performance problems
- Architecture consistency

### 6. Cross-model peer review (optional)

Run **peer-review.md**.

Paste findings from another model (Codex, Gemini). The dev lead verifies each finding rather than accepting blindly.

### 7. Update documentation

Run **document.md**.

Updates CHANGELOG.md and any affected documentation based on actual code changes.

If a prototype exists for the feature, ensure the requirements doc links to it. A working prototype in hand is more valuable than written specs.

## Capturing issues mid-development

Run **create-issue.md** at any point to quickly capture a bug, feature, or improvement. The issue will be formatted as markdown that you can add to your existing plan or use to create a new plan.

## Priority levels

- **P0**: Critical/blocking
- **P1**: High priority
- **P2**: Normal (default)
- **P3**: Low/nice-to-have

## Markdown plan tracking

Plans use emoji status indicators:
- 🟥 To Do
- 🟨 In Progress
- 🟩 Done

Update the plan file as you work to maintain clear progress visibility.

## Learning mode

Run **learning-opportunity.md** when you encounter something you want to understand better. Shifts to teaching mode with three-level explanations (core concept → mechanics → deep dive).
