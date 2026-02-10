# Quick Start: Visual Design

**Time: 15 min**

---

## Step 1: Choose Entry

| Starting Point | Approach |
|----------------|----------|
| Spec only | Generate with Stitch |
| Rough sketch | AI refines |
| Inspiration | Extract and apply |
| Brand exists | Apply tokens |

---

## Step 2: Generate

```
Generate HTML/CSS for this specification:
[paste spec]
```

Or use Stitch directly.

---

## Step 3: Review

Check against spec:
- Layout correct?
- Hierarchy clear?
- All states designed?
- Responsive?

---

## Step 4: Refine

In Figma or directly:
- Adjust colors
- Fix spacing
- Polish typography

---

## Step 5: Extract Tokens

```yaml
colors:
  primary: "#0066FF"
  error: "#DC2626"

typography:
  heading: "Inter, 24px, 700"
  body: "Inter, 16px, 400"

spacing:
  sm: "8px"
  md: "16px"
  lg: "24px"
```

---

## Step 6: Save

```
docs/C-UX-Scenarios/S01-xxx/P01-signup-form.html
docs/D-Design-System/tokens.yaml
```

---

## The Test

Does visual match spec exactly?

If not, update one or the other. Never leave mismatches.

---

## Done

**Next:** [Design Delivery →](10-design-delivery.md)
