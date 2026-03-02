# Execute prototype

Now implement precisely as planned, in full.

## Required inputs before starting

- Approved plan (from create-plan.md)
- Repo path and target branch (if applicable)

## Before starting

Refer to the markdown plan created by create-plan.md. Work through tasks sequentially or as specified by the user.

If you spot something that needs fixing while working on another task, note it in the plan or ask the user whether to address it now or later.

## Component library usage

Reference the component library for implementation:

```bash
# If needed, fetch latest component structure
cd /tmp && rm -rf moha-component-check
git clone --depth 1 https://github.com/moreharvest/moha-component-library.git moha-component-check
```

**Import pattern:**
```tsx
import { ButtonLabel, InputField, Modal } from "@moha/component-library";
```

**Prioritise existing components.** Only create custom components when the library doesn't cover the need.

If the repo can't be fetched, ask the user for a local copy or a component list before proceeding.

## Implementation requirements

- Write clean, readable code sufficient for testing (not production polish).
- Use existing component library components where identified in the plan.
- Adhere to existing code patterns and conventions.
- Include brief comments for non-obvious interactions.
- As you implement each step:
  - Update the markdown tracking document with emoji status and overall progress percentage.

## Prototype mindset

This is a prototype for user testing, not production code. Priorities:
1. **Testable**: The interaction being tested must work reliably
2. **Realistic**: UI should feel real enough for valid user feedback
3. **Minimal**: Only build what's needed to test the hypothesis
4. **Accessible**: Basic accessibility (keyboard nav, screen reader basics)

Do NOT:
- Over-engineer error handling for edge cases we won't test
- Add features beyond the test scope
- Polish animations or micro-interactions unless they're being tested
- Worry about performance optimisation

## After completing each task

Update the markdown plan:
- Change 🟥 to 🟩 for completed items
- Update overall progress percentage
- Note any deviations or design decisions made

Move to the next task. Continue until all tasks are complete or user stops the session.
