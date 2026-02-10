# Quick Start: Functional Components

**Time: 10 min**

---

## Step 1: Identify Patterns

Review your specifications. What appears 3+ times?

- Same button style
- Same card layout
- Same input pattern

---

## Step 2: Extract When

- Appears 3+ times
- Consistent behavior everywhere
- Worth centralizing

---

## Step 3: Document Component

```markdown
## Button Component

### Variants
| Variant | Use Case |
|---------|----------|
| Primary | Main actions |
| Secondary | Alternative |
| Ghost | Tertiary |
| Danger | Destructive |

### States
Default, Hover, Active, Focused, Disabled, Loading

### Props
| Prop | Type | Default |
|------|------|---------|
| variant | string | primary |
| size | string | medium |
| disabled | boolean | false |
| loading | boolean | false |

### Usage Rules
- One primary per screen
- Always has text label
- Min touch target: 44px
```

---

## Step 4: Reference in Specs

```markdown
### Submit Button
- Component: Button (primary, large)
- Label: "Create Account"
```

---

## Step 5: Save

```
docs/D-Design-System/components/button.md
```

---

## Design System Modes

| Mode | Handling |
|------|----------|
| None | Inline in specs |
| Building | Extract to D-Design-System/ |
| Library | Reference external (shadcn) |
| Existing | Import from previous project |

---

## Done

**Next:** [Visual Design →](09-visual-design.md)
