# Developer feedback workflow documentation

## Purpose

Capture complete feedback information upfront to:

- Save time creating GitHub issues manually
- Reduce back-and-forth between product and development
- Ensure developers have everything they need to investigate or implement

## Feedback types

This workflow handles three types of developer feedback:

| Type | Definition | Example |
|------|------------|---------|
| **Bug** | Something is broken or not working as designed | "The login button doesn't respond on iOS" |
| **Re-work** | A missed requirement we should have specified | "We need to support multiple currencies but never included it" |
| **Refactor** | An improvement based on learnings or feedback | "Users find the checkout flow confusing; we should simplify it" |

## How it works

1. Open a chat in the Developer feedback workflow folder
2. Describe your feedback (bug, missed requirement, or improvement)
3. The workflow identifies the type and routes to the appropriate persona
4. Answer the structured questions
5. Review the summary for accuracy
6. Receive GitHub issue URL(s)

## Files in this workflow

| File | Purpose |
|------|---------|
| CLAUDE.md | Triggers the workflow and routes to the correct persona |
| PROBLEM-MANAGER.md | Expert problem manager persona for bugs |
| BUSINESS-ANALYST.md | Expert BA persona for Re-work and Refactor items |
| GITHUB-CONFIG.md | Repository mapping, labels, and issue templates |
| WORKFLOW.md | This documentation |

## Question sequences

### Bugs (Problem Manager)

1. **Platform**: Web, iOS, Android, CMS, Backend/API
2. **Environment**: Development, Staging, or Production
3. **Discovery context**: How the bug was found
4. **Steps to reproduce**: Exact steps to trigger the bug
5. **Expected vs actual**: What should happen vs what happened
6. **Severity**: P0-critical, P1-high, or P2-medium
7. **Platform-specific details**: Device, browser, endpoint, etc.
8. **Evidence**: Screenshots, recordings, logs (when relevant)
9. **Additional context**: Anything else helpful
10. **Confirmation**: Review before issue creation

### Re-work and Refactor (Business Analyst)

1. **Type confirmation**: Re-work or Refactor
2. **Platform**: Web, iOS, Android, CMS, Backend/API
3. **Current state**: What exists today
4. **Desired state**: What the new behaviour should be
5. **Rationale**: Why this change is needed
6. **User impact**: Who is affected
7. **Acceptance criteria**: How we'll know it's complete
8. **Dependencies**: Any constraints or dependencies
9. **Evidence**: Screenshots, feedback, examples
10. **Additional context**: Anything else helpful
11. **Confirmation**: Review before issue creation

## Multiple items per session

You can report multiple items in one chat:

- Each item is numbered (Issue 1, Issue 2, etc.)
- Complete all questions for one item before moving to the next
- Each item creates a separate GitHub issue
- Session ends with a summary of all created issues

## What this workflow does not do

- Suggest root cause or implementation recommendations in the initial issue
- Prioritise items relative to each other
- Assign to anyone other than calmannix

## Maintenance

| To update... | Edit... |
|--------------|---------|
| Bug questions | `PROBLEM-MANAGER.md` |
| Re-work/Refactor questions | `BUSINESS-ANALYST.md` |
| GitHub settings or templates | `GITHUB-CONFIG.md` |
| Routing logic | `CLAUDE.md` |
