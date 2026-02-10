# Quick Start: Storyboarding

**Agent: Freya** | **Time: 10 min**

---

## Start the Dialog

```
You are Freya, a WDS design agent.

I have a sketch of [view name] at keyframe 0 (default state).

Now I need to storyboard the interactions.
What elements on this view can change state?
```

---

## When Freya Identifies Elements

Pick the most important one first:

```
Freya: "The submit button, password field, and error messages
all have state changes."

You: "Let's start with the password field.
Walk me through every keyframe from empty to validated."
```

---

## When Freya Describes States

Ask for the WHY:

```
Freya: "Keyframe 1: User types, characters are masked."

You: "Why masked by default?"

Freya: "Security expectation. But we add a show/hide toggle
because Felix fears typos in passwords."
```

---

## Generate the Storyboard

```
Generate a complete storyboard for [element].

For each keyframe include:
- Keyframe number
- What the user sees
- What triggered this state
- Why this matters to the persona
- Timing (if relevant)
```

---

## Example Output

```markdown
## Password Field Storyboard

### Keyframe 0: Default
- Input empty, placeholder visible
- Eye icon (closed) for show/hide
- No validation message
- WHY: Clean starting point, show/hide visible from start

### Keyframe 1: User Types
- Characters masked as dots
- Strength indicator appears
- Shows "Weak" in red
- WHY: Immediate feedback prevents weak password submission

### Keyframe 2: Password Strong
- Strength indicator full, green
- Shows "Strong"
- Checkmark appears
- WHY: Positive reinforcement, confidence to proceed

### Keyframe 3: Show Password (optional)
- User clicks eye icon
- Characters become visible
- Eye icon opens
- WHY: Felix fears typos, needs to verify
```

---

## Add to Specification

Storyboards become part of your page spec.

---

**Next:** [Conceptual Specifications →](07-conceptual-specifications.md)
