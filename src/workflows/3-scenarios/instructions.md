# Scenarios Workflow - Context-Aware Agent Instructions

**Pattern:** Trigger Map Initiation → Scenario Conversation
**Phase:** 3 (UX Scenarios)
**Primary Agent:** Freya (UX Designer)

---

## On Workflow Invocation

### Step 1: Project State Detection

**Read prerequisite artifacts:**
1. Product Brief: `{output_folder}/A-Product-Brief/product-brief.md`
2. Trigger Map: `{output_folder}/B-Trigger-Map/trigger-map.md`
3. Project Outline: `{project-root}/_bmad/project-outline.md`

**Check for existing work:**
- Look for `{output_folder}/C-UX-Scenarios/` folder
- Check for unfinished agent dialogs in `{project-root}/_bmad/wds/agent-dialogs/`
- Find most recent scenario-related dialog (if any)

### Step 2: Resume or Start Decision

**If unfinished dialog found:**
```
Agent: "I see we started scenario work but didn't finish. Let me pick up where we left off..."
[Read dialog file, continue from last completed task]
```

**If C-UX-Scenarios/ exists with partial content:**
```
Agent: "I see you have [N] scenarios documented. Should I:
1. Continue with remaining scenarios
2. Review and adjust existing scenarios
3. Start fresh"
```

**If starting fresh (Trigger Map complete, no scenarios yet):**
```
[Proceed to Step 3: Mode Selection]
```

### Step 3: Mode Selection

**Read from Trigger Map analysis:**
- Site/app type (presentation vs dynamic)
- Total page/view count
- Complexity indicators

**Select conversation mode:**

**Dialog Mode** — Use when:
- Product scale > 100 pages
- Strategic scoping needed
- Large product requiring selective ignorance

**Suggest Mode** — Use when:
- Medium complexity (20-50 pages)
- Clear structure, needs validation
- Presentation sites with natural groupings

**Dream Mode** — Use when:
- Simple structure (< 20 pages)
- Pattern obvious from Trigger Map
- User trusts autonomous execution

### Step 4: Execute Pattern

**Load patterns from docs/method/:**
1. `trigger-map-initiation.md` — How to initiate scenarios
2. `scenario-conversation-pattern.md` — How to walk through scenarios

**Dialog Mode behavior:**
```
Agent: "Looking at your Trigger Map, I see [site type] with [page count] pages.

What's the most important flow for this type of product?"

[Collaborative discovery, strategic scoping, selective ignorance if needed]
```

**Suggest Mode behavior:**
```
Agent: "Based on your Trigger Map, I'm imagining [N] scenarios:

**Scenario 1: [Purpose]**
- Pages: [list]
- Persona: [name] ([driving force])
- Rationale: [why this grouping]

[Continue for all scenarios...]

Does this make sense?"

[User approves/adjusts → Document scenarios]
```

**Dream Mode behavior:**
```
Agent: "I've created [N] scenarios covering your entire site structure:

**Scenario 1: [Purpose]** — [pages covered]
**Scenario 2: [Purpose]** — [pages covered]

Here's what I documented..."

[Present completed scenarios for review]
```

---

## Principles to Follow

**From trigger-map-initiation.md:**
1. Scenarios expose pages for scrutiny (code hides, scenarios reveal)
2. Force detailed thinking (can't skip details in walkthrough)
3. Learning effect (deep work on critical flows reveals patterns for rest)
4. Share principles, agent makes judgments

**Page documentation strategy:**
- Few pages + high variation → Separate pages
- Many pages + low variation → Template with content variations
- Agent judges based on scale, variation, context

**Coverage strategy:**
- Small sites (20-50 pages) → Comprehensive coverage
- Large products (100s+ pages) → Selective ignorance, focus on critical flow

---

## Agent Dialog Creation

**On workflow start:**
```
Create agent dialog: {project-root}/_bmad/wds/agent-dialogs/[date]-scenarios.md
Track progress with visual status indicators (⏳/✅/⚠️/⏸)
```

**During execution:**
- Log all questions and answers
- Note which documents each answer populates
- Update progress status in REAL-TIME
- Document key decisions with reasoning

**On completion:**
- Complete retrospective before marking workflow complete
- Update project outline
- Link from design-log.md

---

## Output Artifacts

**Folder structure:**
```
C-UX-Scenarios/
├── 00-scenario-overview.md  ← Links to all scenarios
├── 01-[Scenario-Name]/
│   └── 01-[Scenario-Name].md
├── 02-[Scenario-Name]/
│   └── 02-[Scenario-Name].md
└── agent-dialogs/
    └── [date]-scenario-creation.md
```

**Scenario formats:**
- **Screen Flow:** Sequential pages, page-to-page navigation
- **Storyboard:** States within dynamic view, non-linear interactions

---

## Handoff to Next Phase

**On completion:**
```
Agent: "✓ All scenarios documented

Next steps:
- Phase 4: PRD & Platform Requirements
- Phase 5: Design System
- Phase 6: Build

Would you like to continue to Phase 4, or take a break?"
```

---

**Status:** Pattern-driven smart agent
**Created:** 2026-02-12
**Integrates:** trigger-map-initiation.md + scenario-conversation-pattern.md
