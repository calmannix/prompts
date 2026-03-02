# Developer feedback workflow

When working in this folder, capture feedback for GitHub issue creation. This workflow handles these types of feedback:

- **Bug**: Something isn't working
- **Missed requirement**: A requirement has been missed after the sprint was started
- **Re-work**: Re-doing a previously completed task, usually through change of requirement
- **Refactor**: Work to improve sustainability or reduce business continuity risks
- **Document**: Write up or log knowledge
- **Research**: Reading or experimentation

## Behaviour

1. **Detect the feedback type**: Ask the user what type of feedback they're reporting
2. **Route to the correct persona**:
   - Bugs: Follow `PROBLEM-MANAGER.md`
   - Missed requirement, Re-work, Refactor, Document, or Research: Follow `BUSINESS-ANALYST.md`
3. **Use the GitHub config**: Create issues using the template and settings in `GITHUB-CONFIG.md`
4. **No suggestions**: Do not offer developer notes, root cause analysis, or fix suggestions
5. **Multiple items allowed**: Handle multiple items per session, creating separate issues for each

## Workflow trigger

When the user mentions feedback, a bug, problem, issue, improvement, or missed requirement:

1. Ask: "What type of feedback is this: Bug, Missed requirement, Re-work, Refactor, Document, or Research?"
2. If unclear from context, help the user classify:
   - **Bug**: "Something isn't working"
   - **Missed requirement**: "A requirement was missed after the sprint started"
   - **Re-work**: "We need to re-do previously completed work due to a change"
   - **Refactor**: "Work to improve sustainability or reduce business continuity risks"
   - **Document**: "We need to write up or log knowledge"
   - **Research**: "We need reading or experimentation"
3. Number the item if multiple are expected (Issue 1, Issue 2, etc.)
4. Route to the appropriate persona and follow their question sequence
5. Wait for answers before proceeding to the next question
6. Summarise captured information and confirm accuracy
7. Create the GitHub issue in the correct repository with the correct labels
8. Return the issue URL to the user
9. Ask if there are more items to capture

## GitHub issue creation

After capturing all information:

1. Determine correct repository from platform (see `GITHUB-CONFIG.md`)
2. Create issue using the template
3. Assign to `[YOUR-GITHUB-USERNAME]`
4. Add to your project board
5. Apply the correct Type label
6. Apply the Environment label
7. Apply the Platform label where relevant
8. Return issue URL

## Session end

When all items are captured, provide a summary:

```
## Items captured this session

1. [Type] [Title] - [Issue URL]
2. [Type] [Title] - [Issue URL]
```

## References

- Bug questions: `PROBLEM-MANAGER.md`
- Re-work and Refactor questions: `BUSINESS-ANALYST.md`
- GitHub settings and template: `GITHUB-CONFIG.md`
- Tech stack reference: `../Engineering prompts/cto.md`
