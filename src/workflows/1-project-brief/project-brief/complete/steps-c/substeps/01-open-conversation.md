# Substep 1: Open Conversation

## Task

Adapt opening question to project context and invite user to think out loud.

## Instructions

### 1. Check Project Context

Read from `wds-project-outline.yaml`:
- `project_context.stakes` 
- `working_relationship.involvement_level`

### 2. Adapt Opening Question

**DON'T ask:** "What's your vision statement?"

**DO ask (adapt to stakes):**

**If stakes = personal/hobby:**
> "Tell me about this project! What are you building and what excites you about it?"

**If stakes = business:**
> "What are you envisioning? Tell me in your own words about what you want to create - just dump your ideas, I'll help structure them."

**If stakes = departmental/enterprise:**
> "Let's start with the big picture. What problem are you solving, and what does success look like organizationally?"

### 3. Set Expectation

Make it clear this is exploratory:
> "Don't worry about having it all figured out - just share what you're thinking, and I'll help organize it."

---

## Example

**Agent reads context:**
```yaml
project_context:
  stakes: business
working_relationship:
  involvement_level: balanced
```

**Agent opens:**
> "What are you envisioning for this website? Tell me in your own words - just dump your ideas, I'll help structure them. Don't worry if it's not perfectly organized yet."

**User (Björn/Källa):**
> "Well, I just need something that looks professional and stops people from calling about basic stuff I can't help with anyway. We do cars, buses, tractors, everything. Tourists in summer drive me crazy - they break down and need help NOW."

---

## Next

Once conversation is open, load and execute: `02-explore-vision.md`
