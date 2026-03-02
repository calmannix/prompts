# Create Issue

User is mid-development or iterating after testing and thought of a bug/feature/improvement. Capture it fast so they can keep working.

## Your goal

Create a complete issue with:
- Clear title
- TL;DR of what this is about
- Current state vs expected outcome
- Design rationale (why this change improves UX)
- Relevant files/components that need touching
- Risk/notes if applicable
- Proper type/priority/effort labels

## How to get there

**Ask questions** to fill gaps. Be concise, respect the user's time. They're mid-flow and want to capture this quickly. Usually need:
- What's the issue/feature
- Current behaviour vs desired behaviour
- Type (bug/feature/improvement) and priority if not obvious
- What user feedback or test result prompted this (if iteration)

Keep questions brief. One message with 2-3 targeted questions beats multiple back-and-forths.

**Search for context** only when helpful:
- Web search for UX best practices if it's a complex interaction
- Grep codebase to find relevant files
- Check component library for existing solutions
- Note any risks or dependencies you spot

**Skip what's obvious.** If it's a straightforward bug, don't search web. If type/priority is clear from description, don't ask.

**Keep it fast.** Total exchange under 2 minutes. Be conversational but brief. Get what you need, create ticket, done.

## Behaviour rules

- Be conversational: ask what makes sense, not a checklist
- Default priority: P2, effort: medium (ask only if unclear)
- Max 3 files in context: most relevant only
- Bullet points over paragraphs
- Include design rationale for UI changes

## Design context fields

For UI/UX changes, capture:
- **Test finding**: What user feedback or test result prompted this?
- **Design rationale**: Why does this change improve UX?
- **Component impact**: Which components from the library are affected?

## After user confirms

Present the issue in this format:

```markdown
## [Issue Title]

**Type:** [Bug/Feature/Improvement]
**Priority:** [P0/P1/P2/P3]

### TL;DR
[Brief summary]

### Current vs Expected
- Current: [what happens now]
- Expected: [what should happen]

### Design Rationale
[Why this change improves UX]

### Test Finding (if iteration)
[What user feedback or test result prompted this]

### Affected Components
- [Component1](path/to/component1.tsx)
- [Component2](path/to/component2.tsx)

### Component Library Impact
[Which components from @moha/component-library are affected]

### Risks/Notes
[Any dependencies, edge cases, or implementation notes]
```

Confirm: "Issue documented. Add this to your markdown plan or create a new plan if starting fresh."

## Iteration workflow note

For issues created during iteration (after testing):
1. Create the issue here
2. Consult head-of-design.md for design validation
3. Continue with execute.md
4. Review.md is always required
5. Peer-review.md is optional (prompt will advise)
