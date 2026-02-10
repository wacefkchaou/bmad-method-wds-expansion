# Quick Start: Conceptual Specifications

**Agent: Freya** | **Time: 20 min**

---

## Start the Dialog

```
You are Freya, a WDS design agent.

Here's my scenario: [paste scenario-overview.md]
Here's my sketch/storyboard: [paste or describe]

I need a complete specification for [view name].

Go through every element systematically. For each, I'll tell you:
- What it is
- Why it exists
- How it behaves
- What content it shows

Start with the first element.
```

---

## When Freya Asks About an Element

Give her the full picture:

```
Freya: "Tell me about the email input field."

You:
- Type: Text input
- ID: signup-email-field
- Persona: Felix
- Driving force: Fear of complicated forms
- Feature: F03-Quick-Signup
- States: Default, Focused, Filled, Error, Valid
- Label: "Email"
- Placeholder: "you@company.com"
- Error message: "Please enter a valid email"
```

---

## When Freya Asks for Content

Give her REAL copy, not placeholders:

```
Freya: "What's the headline for this page?"

You: "Start building in 2 minutes"
NOT: "Lorem ipsum" or "Headline goes here"
```

---

## When Freya Finds Gaps

Let her challenge you:

```
Freya: "You specified the error state for email but not password.
What happens when password is too short?"

You: "Error message: 'Password must be at least 8 characters'
Red border, message appears below field."
```

---

## Generate the Complete Spec

```
Generate the complete page specification for [view name].

Include:
- Purpose statement
- Persona and trigger connections
- Every element with:
  - Unique ID
  - Type
  - All states
  - Real content
  - Behavior
- Acceptance criteria
```

---

## Review Checklist

Ask Freya to audit:

```
Review this specification for completeness:
- Any elements missing?
- Any states undefined?
- Any placeholder content?
- Can a developer build this without questions?
```

---

## Save

```
docs/C-UX-Scenarios/S01-xxx/P01-signup-form.md
```

---

**Next:** [Functional Components →](08-functional-components.md)
