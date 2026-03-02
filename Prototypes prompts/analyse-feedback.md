# Analyse feedback

Consume test results and measure against success metrics. Produce improvement recommendations.

## Before starting

**Ask the user:**

1. **What format is the feedback in?**
   - Lyssna CSV export
   - Interview notes (pasted or file)
   - Other format (specify)

2. **Do you have the original test plan?**
   - If yes: reference it for success metrics
   - If no: ask user to provide success metrics

Wait for the data before proceeding.

---

## Analysis process

### Step 1: Parse the data

**For Lyssna CSV:**

Lyssna exports have dynamic column structures based on test configuration:
- **Fixed columns**: `Date`, `Duration (ms)`, `Age`, `Country`, `Gender`, `Education level`, `Annual household income`, `Employment status`, demographic fields, `Device Type`, `Device Platform`, `Device Width`, `Device Height`
- **Dynamic columns**: Each task/question generates columns with the pattern `{Task ID} ({Task Type} - {Task Name}) {Detail}` where the full question text appears in the header

To parse:
1. Read the header row to identify question columns (they contain the question text)
2. Map each question column to the corresponding success metric from the test plan
3. If headers don't match expected questions, ask the user to clarify the mapping before continuing
4. Calculate aggregate metrics (completion rates, averages, distributions)

**For interview notes:**
- Identify themes across participants
- Count occurrences of behaviours
- Note direct quotes that illustrate patterns

### Step 2: Measure against success metrics

For each metric from the test plan:

```markdown
### Metric: [Name]

**Target:** [From test plan]
**Actual:** [Calculated from data]
**Verdict:** ✅ Pass / ❌ Fail / ⚠️ Borderline

**Evidence:**
- [Data points supporting this verdict]
- [Relevant quotes or observations]

**Confidence:** High / Medium / Low
- [Why this confidence level: sample size, consistency, etc.]
```

### Step 3: Identify patterns

Look for:
- **Consistent struggles**: Where did multiple participants fail?
- **Unexpected successes**: What worked better than expected?
- **Split opinions**: Where was feedback divided?
- **Outliers**: Any responses that don't fit the pattern?

### Step 4: Generate insights

For each pattern, document:
- What happened
- Why it happened (inferred from data + UX principles)
- What it means for the prototype

---

## Output format

```markdown
# Feedback Analysis: [Test Name]

## Executive summary
- **Overall verdict:** Pass / Fail / Partial pass
- **Key finding:** [One sentence]
- **Recommended action:** Iterate / Pass to dev / Retest

## Metrics scorecard

| Metric | Target | Actual | Verdict |
|--------|--------|--------|---------|
| [Metric 1] | [X] | [Y] | ✅/❌/⚠️ |
| [Metric 2] | [X] | [Y] | ✅/❌/⚠️ |

## Detailed findings

### ✅ What worked
1. **[Finding]**
   - Evidence: [Data]
   - Implication: [What this means]

### ❌ What didn't work
1. **[Finding]**
   - Evidence: [Data]
   - Severity: Critical / High / Medium / Low
   - Implication: [What this means]

### ⚠️ Unclear / needs more data
1. **[Finding]**
   - Evidence: [Data]
   - What we'd need to clarify: [Next step]

## Improvement recommendations

Use severity labels aligned with review.md (CRITICAL / HIGH / MEDIUM / LOW) when classifying issues in findings. Map to priority tiers as follows: CRITICAL/HIGH → Priority 1, MEDIUM → Priority 2, LOW → Priority 3.

### Priority 1: Must fix before production
| Issue | Recommendation | Rationale | Effort |
|-------|----------------|-----------|--------|
| [Issue] | [Fix] | [Why] | Low/Med/High |

### Priority 2: Should fix
| Issue | Recommendation | Rationale | Effort |
|-------|----------------|-----------|--------|
| [Issue] | [Fix] | [Why] | Low/Med/High |

### Priority 3: Consider for future
| Issue | Recommendation | Rationale | Effort |
|-------|----------------|-----------|--------|
| [Issue] | [Fix] | [Why] | Low/Med/High |

## Next steps

**If iterating:**
- [ ] Create issues for Priority 1 fixes (use create-issue.md)
- [ ] Consult Head of Design on approach (use head-of-design.md)
- [ ] Implement fixes (use execute.md)
- [ ] Retest with design-test.md

**If passing to dev team:**
- [ ] Document final design decisions
- [ ] Create production requirements based on validated prototype
- [ ] Note any compromises made for prototype that need production polish
```

---

## Head of Product Design perspective

When generating recommendations, think like the Head of Product Design:

- **Prioritise ruthlessly**: Not everything needs fixing. Focus on what affects the core hypothesis.
- **Evidence-based**: Every recommendation ties back to user data, not opinion.
- **Feasibility-aware**: Consider effort vs impact. A 2-hour fix that solves 80% of issues beats a 2-week rebuild.
- **Test validity**: Will the fix actually address the user problem, or are we pattern-matching?

## Decision framework

**Pass to dev team when:**
- All critical metrics pass
- No severe usability issues remain
- Design is validated for production

**Iterate when:**
- Critical metrics fail
- Clear, fixable issues identified
- Iteration effort is reasonable (< re-testing cost)

**Retest when:**
- Sample size too small for confidence
- Results are ambiguous
- Major changes invalidate previous results

**Pivot when:**
- Fundamental hypothesis is wrong
- User problem is different than assumed
- Multiple iterations haven't improved metrics
