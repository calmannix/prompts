# GitHub configuration for developer feedback

Configure this file for your organisation before using the workflow.

## Your configuration

Replace these placeholders before using:

| Placeholder | Replace with |
|-------------|-------------|
| `[YOUR-ORG]` | Your GitHub organisation or username |
| `[YOUR-REPO]` | Your primary app repository |
| `[YOUR-GITHUB-USERNAME]` | Your GitHub username |
| `[YOUR-PROJECT-NUMBER]` | Your GitHub project board number |

## Repository mapping

Map platforms to repositories based on your project structure. Example:

| Platform | Repository |
|----------|------------|
| Web App | `[YOUR-ORG]/[YOUR-REPO]` |
| iOS | `[YOUR-ORG]/[YOUR-REPO]` |
| Android | `[YOUR-ORG]/[YOUR-REPO]` |
| Backend / API | `[YOUR-ORG]/[YOUR-REPO]` |
| Website | `[YOUR-ORG]/website` |
| CMS | `[YOUR-ORG]/cms` |

## Labels

### Type labels (apply one)
- `Bug`
- `Missed requirement`
- `Re-work`
- `Refactor`
- `Document`
- `Research`

### Environment labels (apply one)
- `Dev`
- `Staging`
- `Prod`

### Platform labels (apply one where relevant)
Customise to match your platforms.

## Priority

| Priority | Use for |
|----------|---------|
| P1 | Blocker bugs |
| P2 | Refactors, missed requirements, non-blocking bugs |
| P3 | Design or aesthetic issues |

## Issue creation checklist

- [ ] Correct repository selected
- [ ] Type label applied
- [ ] Environment label applied
- [ ] Platform label applied (where relevant)
- [ ] Priority set
- [ ] Assigned to `[YOUR-GITHUB-USERNAME]`
- [ ] Added to project board
- [ ] No developer notes or implementation suggestions in the initial issue
- [ ] Each item gets its own issue

## Issue templates

### Bug template

```markdown
## Summary

[One sentence description]

## Steps to reproduce

1. [Step 1]
2. [Step 2]
3. [Step 3]

## Expected behaviour

[What should happen]

## Actual behaviour

[What happened instead]

## Environment

- **Environment**: [Development / Staging / Production]
- **Platform**: [Your platforms]
- **Found during**: [Normal use / Testing / User-reported]
- **Date**: [YYYY-MM-DD]

### Platform details

[Device, OS version, browser, endpoint — as relevant]

## Evidence

[Screenshots, logs, or error messages]

## Additional context

[Did it work before? How often does it occur?]
```

### Missed requirement, Re-work, Refactor, Document, and Research template

```markdown
## Summary

[One sentence description]

## Type

- **Category**: [Missed requirement / Re-work / Refactor / Document / Research]
- **Platform**: [Your platforms]

## Current state

[What exists today, or "Not implemented"]

## Desired state

[What the new behaviour should be]

## Rationale

[Why this is needed. What learning or gap drove this?]

## User impact

- **Affected users**: [User types or roles]
- **Scope**: [All users / Specific segment]

## Acceptance criteria

- [ ] [Testable criterion 1]
- [ ] [Testable criterion 2]
- [ ] [Testable criterion 3]

## Evidence

[Screenshots, user feedback, analytics, or examples if available]
```
