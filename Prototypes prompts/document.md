# Update Documentation Task

You are updating documentation after code changes.

## 0. Prototype link (if applicable)

If a prototype exists for this feature, link it at the top of any requirements or BDD doc.

A working prototype in hand is more valuable than written specs. Engineers should interact with the prototype before reading requirements.

## 1. Identify changes

- Check git diff or recent commits for modified files
- Identify which features/modules were changed
- Note any new files, deleted files, or renamed files

## 2. Verify current implementation

**CRITICAL**: DO NOT trust existing documentation. Read the actual code.

For each changed file:
- Read the current implementation
- Understand actual behaviour (not documented behaviour)
- Note any discrepancies with existing docs

## 3. Update relevant documentation

- **CHANGELOG.md**: Add entry under "Unreleased" section
  - Use categories: Added, Changed, Fixed, Security, Removed
  - Be concise, user-facing language

## 4. Documentation style rules

✅ **Concise** - Sacrifice grammar for brevity
✅ **Practical** - Examples over theory
✅ **Accurate** - Code verified, not assumed
✅ **Current** - Matches actual implementation

❌ No enterprise fluff
❌ No outdated information
❌ No assumptions without verification

## 5. Handling unknowns

**Never guess. Never make things up.**

If something is undefined:
- API contracts: mark as "TBD: ask PM"
- Database schema: mark as "TBD: ask PM"
- Complex logic: flag as separate ticket or "TBD: ask PM"
- Integration details: mark as "TBD: ask PM"

Example:
```markdown
## Backend

**Endpoint:** TBD: ask PM
**Database:** TBD: requires schema discussion
```

## 6. Ask if uncertain

If you're unsure about intent behind a change or user-facing impact, **ask the user**: don't guess.