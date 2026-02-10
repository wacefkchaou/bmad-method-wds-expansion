# Quick Start: Outline Scenarios

**Agent: Freya** | **Time: 10 min**

---

## Start the Dialog

```
You are Freya, a WDS design agent.

Here's my Trigger Map:
[paste trigger-map.md content]

I need to outline scenarios for each persona.
A scenario is the sunshine path — shortest route from current state to desired state.

Start with [persona name]. What's their primary goal?
```

---

## When Freya Asks About the Goal

Tell her:
- Where the persona starts (current state)
- Where they want to end (desired state)
- What value this creates (for user AND business)

**Example response:**
```
Current: New user on landing page, curious but uncommitted
Desired: Registered user, welcomed, ready to use the app
User value: Has an account, feels confident
Business value: New user in activation funnel
```

---

## When Freya Asks About the Flow

Map the logical views in order:

```
Freya: "What steps does the user take?"

You:
1. Landing page — sees value prop, clicks CTA
2. Signup form — enters email and password
3. Welcome screen — confirmed, ready to explore
```

**Keep it linear.** No branches. No "what if" yet.

---

## When Freya Asks About Edge Cases

```
Freya: "What if the email is already registered?"

You: "That's an edge case. Document it separately.
Right now I want the sunshine path only."
```

---

## Generate the Scenario

```
Generate a scenario outline for [persona] achieving [goal].

Use this format:
- Scenario ID and name (S01-User-Registration)
- Current state
- Desired state
- Value check (user + business)
- Linear flow (numbered steps)
- Connections to features and triggers
```

---

## Save

```
docs/C-UX-Scenarios/S01-User-Registration/scenario-overview.md
```

---

**Next:** [Conceptual Sketching →](05-conceptual-sketching.md)
