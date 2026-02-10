# Quick Start: Trigger Mapping

**Agent: Saga** | **Time: 15 min**

---

## Start the Dialog

```
You are Saga, a WDS strategic analyst.

Here's my Project Brief:
[paste project-brief.md content]

I need to create a Trigger Map. Help me identify:
1. Personas — who are the 2-4 user types
2. Driving forces — what makes each persona act
3. Features — what capabilities address these forces

Start with personas. Ask me questions to draw them out.
```

---

## When Saga Asks About Personas

Describe real people you know or can imagine:
- What's their role?
- What's their day like?
- What frustrates them?

**Example response:**
```
There's the busy parent who works full-time.
They feel guilty about the dog.
They want to make sure the dog is cared for without adding mental load.
```

---

## When Saga Asks About Driving Forces

For each persona, tell her:

| Force | Question to Answer |
|-------|-------------------|
| **Fears** | What are they afraid of? |
| **Desires** | What do they want? |
| **Frustrations** | What annoys them today? |
| **Motivations** | What would make them act? |

**Example response:**
```
Fear: The dog isn't getting enough exercise
Desire: Peace of mind that someone handled it
Frustration: Asking "did anyone walk the dog?" every day
Motivation: Seeing the family work as a team
```

---

## When Saga Asks About Features

Connect each driving force to a capability:

```
Saga: "What feature addresses the fear of the dog not getting exercise?"

You: "A visible log showing all completed walks with times."
```

---

## Generate the Document

```
Generate the complete Trigger Map as markdown.

Include:
- Persona profiles with names
- Driving forces per persona
- Feature list with connections to driving forces
- Priority ranking
```

---

## Save

```
docs/B-Trigger-Map/trigger-map.md
```

---

**Next:** [Platform Requirements →](03-platform-requirements.md)
