# Quick Start: Product Evolution

**Agent: Idunn** | **Time: 10 min**

---

## Start the Dialog

```
You are Idunn, a WDS implementation partner.

The product is live. Now we need to evolve it.

Current state:
- Project Brief: [paste or reference]
- Trigger Map: [paste or reference]
- Live product URL: [url]

Help me plan the next iteration.
```

---

## When Planning New Features

Connect back to strategy:

```
Idunn: "What new feature are you considering?"

You: "Users are requesting bulk actions."

Idunn: "Which persona does this serve?
What driving force does it address?"

You: "Felix — frustration with repetitive tasks."
```

---

## When Updating Existing Features

Start with the spec:

```
I need to update [feature name].

Current spec: [paste or reference]
Requested change: [describe]

What's the impact on:
- Other features?
- User flows?
- Acceptance criteria?
```

---

## When Fixing Bugs

Document the gap:

```
Bug report: [describe issue]
Expected behavior (from spec): [what spec says]
Actual behavior: [what happens]

Is this a spec gap or implementation bug?
```

---

## Evolution Workflow

```
New request
    ↓
Connect to Trigger Map
    ↓
Update spec (with Freya if needed)
    ↓
Build (with Idunn)
    ↓
Test against spec
    ↓
Deploy
    ↓
Document in Agent Dialog
```

---

## Keep Documents Current

After each change:

```
Update the following:
1. Spec file if behavior changed
2. Acceptance criteria if new cases
3. Agent Dialog with decisions made
4. Trigger Map if new driving forces discovered
```

---

## Track Evolution

```
Create: docs/F-Agent-Dialogs/YYYY-MM-DD-feature-update/

Include:
- What changed
- Why (driving force)
- Impact on other features
- Decisions made
```

---

## The Living Product

Products don't end at launch.

Every change:
- Traces back to user psychology
- Updates specifications
- Gets tested against spec
- Gets documented

---

## Done

Keep evolving.
