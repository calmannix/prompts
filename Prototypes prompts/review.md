# Prototype review task

Perform comprehensive review of the prototype. Check both code quality and UI/UX. Be thorough but concise.

## Required inputs before starting

- Prototype repo path and target branch
- Test hypothesis and success metrics (from test plan)
- Component library usage expectations (if any)

## Code checks

**Error handling**: Try-catch for async operations, helpful error states for users
**TypeScript**: No `any` types, proper interfaces, no @ts-ignore
**Component usage**: Using library components correctly, props passed properly
**Test readiness**: Prototype works reliably for testing scenarios
**Architecture**: Code organised logically, easy to modify after testing

## UI/UX checks

**Accessibility**:
- Keyboard navigation works for core flows
- Focus states visible
- Screen reader can parse main content
- Colour contrast meets WCAG AA minimum

**Interaction patterns**:
- Buttons/links have appropriate touch targets (min 44px)
- Loading states exist where needed
- Error states are clear and actionable
- User flow matches the test plan

**Visual consistency**:
- Component library used consistently
- Spacing and typography follow design system
- No jarring custom styles that break consistency

**Test validity**:
- Prototype is realistic enough for valid feedback
- Test hypothesis can be evaluated with this implementation
- No placeholder content that would confuse testers

## Output format

### ✅ Ready for testing
- [Item 1]
- [Item 2]

### ⚠️ Issues found
- **[Severity]** [File:line] - [Issue description]
  - Fix: [Suggested fix]

### 🎨 UX observations
- [Observation about UX that may affect test validity]

### 📊 Summary
- Files reviewed: X
- Critical issues: X
- UX concerns: X
- Test readiness: Ready / Needs fixes

## Severity levels

- **CRITICAL**: Blocks testing, crashes, accessibility failures
- **HIGH**: Affects test validity, confusing UX, broken interactions
- **MEDIUM**: Code quality, minor UX issues
- **LOW**: Polish, minor improvements

## Test validity check

Before approving, verify:
- [ ] Core test flow works end-to-end
- [ ] No placeholder text that reveals it's a prototype
- [ ] Interactions feel realistic enough for valid feedback
- [ ] Success metrics can be measured with this implementation

## Task hygiene

If you find issues that require fixes, document them via create-issue.md and add to your markdown plan before making changes.
