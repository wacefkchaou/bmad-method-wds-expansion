# Quick Start: Agentic Development

**Agent: Idunn** | **Time: 15 min**

---

## Start the Dialog

```
You are Idunn, a WDS implementation partner.

I have a design delivery ready to build.
Specification: [paste page spec]

Help me build this element by element.
We'll compare each piece to the spec as we go.
Start with the most important element.
```

---

## When Idunn Suggests an Approach

Verify it matches the spec:

```
Idunn: "I'll implement the password field with real-time validation
that checks on each keystroke."

You: "The spec says validate on blur, not keystroke.
Let's stick to the spec unless there's a good reason to change."
```

---

## When Implementation Differs from Spec

Decide and document:

```
Idunn: "The spec says red text for errors, but I think a red box
has better contrast for accessibility."

You: "Good point. Let's use the red box.
Document this as a spec change with the reason."
```

---

## Document Decisions

Ask Idunn to track:

```
Add this to the dialog document:

## Decision: Error Display Style
- Spec said: Red text
- Built as: Red box with text
- Reason: Better accessibility contrast
- Spec impact: Update error state description
```

---

## Track Changes from Spec

```
Update the changes log:

| Element | Spec Said | Built As | Reason |
|---------|-----------|----------|--------|
| Error msg | Red text | Red box | A11y contrast |
```

---

## Build Order

Tell Idunn your priority:

```
Let's build in this order:
1. Core happy path — the form works end to end
2. Error states — validation and error messages
3. Edge cases — duplicate email, network errors
4. Polish — loading states, animations

One element at a time. Verify each before moving on.
```

---

## Create the Agent Dialog File

```
docs/F-Agent-Dialogs/YYYY-MM-DD-feature-name/
├── dialog.md           ← The conversation summary
├── decisions.md        ← What was decided and why
└── changes.md          ← Differences from spec
```

---

## Why Document?

- You'll forget why decisions were made
- New team members need context
- Next AI session can load the dialog and continue

---

**Next:** [Testing →](12-testing.md)
