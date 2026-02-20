---
name: 'workflow-conceptualize'
description: 'Collaboratively explore what a scenario's design should achieve before committing to specific pages or layouts.'
---

# [C] Conceptualize — Explore What the Design Needs

**Goal:** Collaboratively explore what a scenario's design should achieve before committing to specific pages or layouts.

**When to use:** When the user isn't sure what pages are needed, wants to think through the user journey, or needs to explore design options before building.

---

## Entry

Load scenario context (VTC, scenario overview) from `{output_folder}/C-UX-Scenarios/`.

## Steps

Execute steps in `./steps-c/`:

| Step | File | Purpose |
|------|------|---------|
| 01 | step-01-exploration.md | Open-ended design exploration |

**Reference data:**
- `./data/scenario-init/` — scenario initialization guides
- `./data/page-creation-flows/` — page creation flow options

---

## After Completion

Return to scenario dashboard (workflow.md) or proceed to:
- **[S] Suggest** — to start building the scenario step by step
- **[P] Specify** — to detail a specific page
