# prompts

Claude prompts and workflows for product, engineering, and prototyping.

These are the actual prompts I use day-to-day. Each folder is a self-contained workflow — open the folder as a project in Claude, and the prompts guide the session.

---

## Workflows

### Developer feedback workflow
Captures bugs, missed requirements, re-work, and refactors as structured GitHub issues. Routes to the right persona (Problem Manager for bugs, Business Analyst for everything else) and creates the issue with correct labels and template.

### Engineering prompts
A step-by-step workflow for AI-assisted development. Covers exploration, planning, execution, code review, peer review, and documentation. Uses markdown plan files with emoji status tracking.

### Prototypes prompts
Same structure as Engineering, extended for prototype work. Adds design leadership, user test planning, and feedback analysis. Built around the principle that a working prototype is worth more than a written spec.

---

## Global files

| File | Purpose |
|------|---------|
| `CLAUDE.md` | Project-level instructions applied across all workflows |
| `WRITING-PREFERENCES.md` | Style guide for all written output |
| `RTF-FRAMEWORK.md` | Prompt evaluation framework (Role, Task, Format) |

---

## Setup

1. Clone or download this repo
2. Open a workflow folder as a project in Claude
3. Customise `[PLACEHOLDER]` values in `cto.md` and `GITHUB-CONFIG.md` for your stack and org
4. Start with the `CLAUDE.md` or `README.md` in each workflow folder
