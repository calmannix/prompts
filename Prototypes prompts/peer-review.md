# Peer review (optional)

A different team lead within the company has reviewed the current prototype and provided findings below. Important context:

- **They have less context than you** on this project's history and decisions
- **You are the team lead**: don't accept findings at face value
- Your job is to critically evaluate each finding

## When to use peer review

**Use peer review when:**
- Significant UI/UX changes that affect the test hypothesis
- New interaction patterns not previously used
- Complex user flows with multiple paths
- Changes that affect accessibility
- You're uncertain about a design decision

**Skip peer review when:**
- Minor copy changes
- Small visual tweaks (spacing, colours)
- Bug fixes that don't change the interaction
- Iterations based on clear test feedback

If unsure, the rule is: if the change could invalidate test results or confuse users, get peer review.

---

Findings from peer review:

[PASTE FEEDBACK FROM OTHER MODEL]

---

## For EACH finding above

### Code findings

1. **Verify it exists**: Actually check the code. Does this issue/bug exist?
2. **If it doesn't exist**: Explain clearly why (maybe it's already handled, or they misunderstood the implementation)
3. **If it does exist**: Assess severity and add to your fix plan

### Design findings

1. **Verify the concern is valid**: Does this UX issue affect test validity?
2. **Check against test hypothesis**: Does fixing this matter for what we're testing?
3. **If valid and relevant**: Add to fix plan with design rationale
4. **If valid but out of scope**: Note for future iteration, don't fix now

### Accessibility findings

1. **Verify against WCAG**: Is this a standard we need to meet?
2. **Check impact on testers**: Will this exclude users from testing?
3. **If blocking**: Fix before testing
4. **If minor**: Note for production version

## After analysis, provide

Use severity labels aligned with review.md (CRITICAL / HIGH / MEDIUM / LOW) when classifying issues.

### Summary of valid findings
Confirmed issues that need fixing before testing:
- [Finding] - [Severity] - [Why it matters for testing]

### Summary of invalid findings
Issues that don't apply or are out of scope:
- [Finding] - [Why it's not applicable]

### Design recommendations
UX improvements worth considering:
- [Recommendation] - [Rationale] - [Implement now / Save for iteration]

### Prioritised action plan
1. [Most critical fix]
2. [Next priority]
3. ...
