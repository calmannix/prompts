# Design test

Create a test plan with questions, tasks, and success metrics for the prototype.

## Before starting

**Ask the user:**

1. **What test methodology are you using?**
   - Lyssna panel (remote, async)
   - Face-to-face interview
   - Other (specify)

2. **What's your sample size?**
   - Lyssna: typically 20-50 responses for quantitative, 5-10 for qualitative
   - Face-to-face: typically 5-8 participants

3. **Who is the target audience?**
   - Demographics, experience level, relationship to product

Wait for answers before generating the test plan.

---

## Test plan structure

### Hypothesis
Restate what we're testing in clear terms:
- "We believe [change] will [outcome] because [reason]"

### Test type determination
Based on the hypothesis, determine whether each question/task needs:

**Quantitative measurement** (use when):
- Testing task completion (can they do it?)
- Measuring preference between options
- Assessing findability or speed
- Need statistical confidence

**Qualitative exploration** (use when):
- Understanding "why" behind behaviour
- Exploring mental models
- Gathering improvement ideas
- Testing comprehension

---

## Output format by methodology

### Lyssna panel format

<format type="lyssna">
## Test: [Name]

### Hypothesis
[What we're testing]

### Participant criteria
- [Criterion 1]
- [Criterion 2]

### Questions/Tasks

#### Task 1: [Name]
**Type:** First-click / Five-second / Preference / Open-ended
**Question:** [Exact question text]
**Success metric:** [What constitutes pass]
**Threshold:** [e.g., 70% correct, average rating > 3.5]

#### Task 2: [Name]
...

### Follow-up questions
1. [Open-ended question to understand reasoning]
2. [Scale question: 1-5 or 1-7]
3. [Multiple choice if needed]

### Success criteria summary
| Metric | Target | Fail threshold |
|--------|--------|----------------|
| [Metric 1] | [Target] | [Below this = fail] |
| [Metric 2] | [Target] | [Below this = fail] |
</format>

### Face-to-face interview format

<format type="face_to_face">
## Test: [Name]

### Hypothesis
[What we're testing]

### Participant criteria
- [Criterion 1]
- [Criterion 2]

### Interview guide

#### Warm-up (2-3 min)
- [Rapport-building question]
- [Context-setting question about their experience]

#### Core tasks (15-20 min)

**Task 1: [Name]**
- Instruction: [What to ask them to do]
- Observe: [What to watch for]
- Probe questions:
  - [If they struggle: "What were you expecting to happen?"]
  - [If they succeed: "What made that easy/hard?"]
- Success indicator: [Observable behaviour that = success]

**Task 2: [Name]**
...

#### Debrief (5-10 min)
- Overall impression: "How would you describe this experience?"
- Comparison: "How does this compare to [alternative/current]?"
- Improvement: "If you could change one thing, what would it be?"

### Observation checklist
| Behaviour | Observed? | Notes |
|-----------|-----------|-------|
| [Specific behaviour to watch] | Y/N | |
| [Hesitation points] | Y/N | |
| [Error recovery] | Y/N | |

### Success criteria summary
| Metric | Target | How measured |
|--------|--------|--------------|
| Task completion | X/Y participants | Observation |
| Comprehension | Correct explanation | Verbal response |
| Satisfaction | Positive sentiment | Debrief responses |
</format>

---

## Success metrics guidance

### Quantitative metrics (typical thresholds)

| Metric type | Good | Acceptable | Fail |
|-------------|------|------------|------|
| Task completion rate | >85% | 70-85% | <70% |
| First-click accuracy | >70% | 50-70% | <50% |
| Preference (A vs B) | >65% | 50-65% | <50% |
| Likert scale (1-5) | >4.0 | 3.5-4.0 | <3.5 |
| Likert scale (1-7) | >5.5 | 4.5-5.5 | <4.5 |
| Time on task | Within expected | 1.5x expected | >2x expected |

### Qualitative indicators

| Indicator | Positive signal | Negative signal |
|-----------|-----------------|-----------------|
| Verbal feedback | "This makes sense", "Easy" | "Confusing", "I don't know" |
| Body language | Leaning in, nodding | Frowning, leaning back |
| Task approach | Direct path, confidence | Wandering, hesitation |
| Error recovery | Self-corrects quickly | Gives up, asks for help |

---

## Before finalising

Verify the test plan:
- [ ] Hypothesis is clear and testable
- [ ] Questions/tasks directly test the hypothesis
- [ ] Success metrics have clear pass/fail thresholds
- [ ] Sample size is appropriate for methodology
- [ ] Questions are unbiased (not leading)
- [ ] Time estimate is realistic for participants
