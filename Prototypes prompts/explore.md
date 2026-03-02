# Initial exploration stage

Your task is NOT to implement this yet, but to fully understand and prepare.

## Your responsibilities

- Analyse and understand the prototype requirements thoroughly.
- Research UI/UX best practices and patterns from the web relevant to this prototype.
- Fetch and catalogue the component library to identify which components fit.
- Determine exactly how this prototype should work, including user flows, interactions, and edge cases.
- Identify anything unclear or ambiguous in the description.
- Push back if requirements are insufficient for good UX. Ask for more context.
- List all questions or ambiguities you need clarified.

Remember, your job is not to implement yet. Explore, research, plan, then ask questions to ensure all ambiguities are covered. We will go back and forth until you have no further questions. Do NOT assume any requirements or scope beyond explicitly described details.

## Research capabilities

You can and should search the web for:
- UI/UX patterns relevant to the prototype (e.g., "best practices for onboarding flows")
- Accessibility guidelines (WCAG, platform-specific)
- Competitor or industry examples
- Interaction patterns that support the test hypothesis

Cite sources when referencing external patterns. Recommend approaches based on evidence, not assumptions.

If web access is unavailable, ask the user to provide sources or proceed with a summary noting the lack of citations.

## Component library research

Fetch the MoreHarvest component library and identify available components:

```bash
# Clone or update the component library
cd /tmp && rm -rf moha-component-check
git clone --depth 1 https://github.com/moreharvest/moha-component-library.git moha-component-check

# List available components
find /tmp/moha-component-check/src/components -name "*.tsx" | sort
```

**Component structure (atomic design):**
- **Atoms**: buttons, icons, labels, inputs, cards, modals, dividers, messages, loading states
- **Molecules**: lists, info cards, graphs, carousels, dropdowns, radio groups, search, text blocks
- **Organisms**: complex cards, carousels, chips, FAQ sections

After fetching, create a component selection list:
- Which existing components fit the prototype requirements
- Which components need minor adaptation
- Which interactions require custom implementation

If the repo can't be fetched, ask the user for a local copy or a component list.

## Greenfield prototypes

For new prototypes with no existing codebase:

- Research proven UI/UX approaches (use web search)
- Recommend interaction patterns based on test hypothesis
- Identify which component library pieces to use
- Propose user flow and screen structure
- Surface decisions that need user input before planning begins

Don't ask the user to choose patterns. Recommend the right approach for their needs.

## UX quality gates

Before proceeding, verify:
- [ ] Test hypothesis is clear and specific
- [ ] User flow is defined (start to end)
- [ ] Success metrics are measurable
- [ ] Component library covers most needs
- [ ] Accessibility requirements are identified
- [ ] Edge cases are documented

If any gate is unclear, ask questions before moving to planning.

## Confirmation

Confirm that you fully understand and I will describe the prototype hypothesis and requirements in detail.
