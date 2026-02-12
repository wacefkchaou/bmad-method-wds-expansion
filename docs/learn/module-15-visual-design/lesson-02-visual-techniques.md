# Module 15: Visual Design

## Lesson 2: Visual Design Techniques

**Practical methods for generating and refining visuals**

---

## Three Methods

In WDS, visual design happens through three categories of tools. You'll likely use a combination depending on the task.

### 1. Figma — Precision Design

Figma is where you go for pixel-level control. In WDS, you don't live in Figma — but you visit it when the agent can't get the details right.

**How you get code into Figma:**

**code.to.design** — a plugin that imports your HTML prototypes directly into Figma as editable layers. Your working prototype becomes a Figma file you can manipulate with all the precision Figma offers. When you're done, export back to code.

**How Figma talks to your agent:**

**Figma MCP** — connects your AI coding agent directly to Figma. The agent can read your Figma designs, extract styles, colors, spacing, and typography, and apply them to code — without you manually exporting or copying values.

**Best for:**
- Fine-tuning visual details the agent can't get right
- Establishing the visual language for a project
- Working with brand elements that need a designer's eye
- Exploring visual directions before committing to code
- Handing off precise specifications to developers

---

### 2. Image Generators — Visual Concepts and Inspiration

AI image generation creates visuals — mood boards, concept art, design inspiration — that inform your design direction. These aren't working code. They're visual reference material that feeds into your specifications and guides the coding agent.

**Nanobanana MCP (Gemini 2.5 Flash Image)** — generates images directly from your AI coding agent and saves them to your repository. We've tested this and it works well for generating visual concepts, mood boards, and design inspiration within your workflow. The images land right in your project folder.

**Best for:**
- Generating mood boards and visual direction
- Creating inspiration images for specifications
- Exploring visual concepts before building
- Communicating visual intent to stakeholders

---

### 3. UI Generators — Working Interfaces from Prompts

UI generators produce working interfaces — real HTML/CSS/React that you can interact with in the browser. This is the core WDS workflow.

**AI code generation (Claude, GPT, etc.)** — the agent generates working code directly from your specifications. You give it a spec, it builds a prototype. You click buttons, fill in forms, see hover states. This is real code, not a picture.

```
You: "Build the signup form from spec P02. Use our design tokens.
      Primary #0066FF, Inter font, 8px spacing scale."

Agent: Creates working HTML/CSS with all elements,
       states, and interactions from the spec.

You: Open in browser. Review. Give feedback.
```

**Google Stitch** — Google has released an API and MCP specifically for generating UI designs and working interfaces. This is designed for producing UI components and page layouts. We have not tested this yet, but it's a promising tool for UI generation alongside the standard code generation workflow.

**Best for:**
- Building working prototypes from specifications
- Iterating on layout, structure, and behavior
- Creating the production foundation
- Testing interactions and responsive behavior

---

## This Is Evolving

We are actively exploring these techniques as tools and capabilities develop rapidly. New image generation models, UI-specific generators, and Figma integrations appear regularly.

**What we've tested:**
- Nanobanana MCP for image generation — works, saves directly to repo
- code.to.design for Figma round-trips — established workflow
- Figma MCP for reading designs into code — works
- AI code generation (Claude, GPT) for UI building — core WDS workflow

**What we're exploring:**
- Google Stitch for UI generation — released API and MCP, not yet tested
- Emerging tools for design-to-code and code-to-design workflows

**Share your experience:** If you discover techniques that work well, or tools we haven't covered, share them in the Discord forum **#UX-design-channel**. This course evolves based on what the community learns together.

---

## Prompting for Visual Output

Whether you're generating code, images, or Figma designs, the quality of your output depends on the quality of your input.

### Prompt Structure for Code Generation

```
Generate [element type] based on this specification:

[Paste your specification]

Visual requirements:
- Font: [font family]
- Primary color: [hex code]
- Background: [color/style]
- Size: [dimensions or responsive]

Focus on: [what's most important]
```

### Example

```
Generate a signup form based on this specification:

## Signup Form
- Email field (required, validates email format)
- Password field (required, 8+ chars, show/hide toggle)
- Submit button: "Create Free Account"
- Terms link below
- Login link for existing users

Visual requirements:
- Font: Inter
- Primary color: #0066FF
- Background: White with subtle gray (#F9FAFB)
- Size: Mobile-first (max-width 400px)

Focus on: Clean, minimal, low friction
```

### Prompt Tips for Image Generation

When generating visual concepts or mood boards:

- Describe the feeling, not just the elements ("warm, inviting, professional" not just "signup form")
- Reference styles ("in the style of Stripe's marketing pages")
- Specify what you'll use the image for ("mood board for the onboarding flow")
- Include constraints ("mobile-first, accessible, brand colors #0066FF and #1A1A2E")

---

## Refining Generated Output

AI output is a starting point, not a final product. Regardless of which method you used, here's what to check and refine.

### Spacing

- AI often under- or over-spaces
- Adjust for visual rhythm
- Ensure breathing room around elements

### Typography

- Check font weights
- Verify line heights
- Adjust size hierarchy

### Colors

- Verify contrast ratios
- Check hover states
- Ensure consistency with tokens

### Touch Targets

- Buttons 44px minimum
- Adequate spacing between tap targets
- Test on actual devices

---

## Designing States

Each interactive element needs its states designed:

### Default

The initial appearance. What users see on load.

### Hover

Feedback on mouseover:
- Slight color change (10% darker)
- Subtle shadow or elevation
- Cursor change

### Active/Pressed

Feedback on click:
- Darker than hover
- Slight scale down (98%)
- Pressed appearance

### Focus

For keyboard navigation — must be visible:
- Outline (2px solid)
- Offset from element
- Sufficient contrast

### Disabled

When interaction is blocked:
- Reduced opacity (50-60%)
- No hover effects
- Cursor: not-allowed

### Loading

During async operations:
- Spinner or skeleton
- Reduced interactivity
- Progress indication

### Error

When something fails:
- Error color (usually red)
- Clear message
- Recovery path visible

---

## Accessibility in Visual Design

### Color Contrast

- Text on background: 4.5:1 minimum (WCAG AA)
- Large text (18px+): 3:1 minimum
- UI components: 3:1 minimum

**Tools:** Contrast checkers in Figma, browser extensions

### Focus Visibility

- Focus rings must be visible
- 3:1 contrast against background
- Don't hide on mouse use

### Touch Targets

- Minimum 44x44px for touch
- 24x24px for precise mouse input
- Adequate spacing between targets

---

## Consistency Patterns

### Token Application

Apply tokens consistently:

```css
/* All primary buttons use same color */
.btn-primary {
  background: var(--color-primary);
  color: var(--color-text-on-primary);
}

/* All headings use same scale */
h1 { font: var(--type-heading-1); }
h2 { font: var(--type-heading-2); }

/* All spacing uses same scale */
.card { padding: var(--space-lg); }
.stack > * + * { margin-top: var(--space-md); }
```

### Component Reuse

Same component, same styling:
- Buttons look identical across pages
- Inputs behave the same everywhere
- Cards have consistent structure

---

## Visual Design Checklist

For each page:

- [ ] Layout matches specification
- [ ] Visual hierarchy correct (primary element dominates)
- [ ] Typography applied from tokens
- [ ] Colors from palette/brand
- [ ] Spacing consistent (uses token scale)
- [ ] All states designed (default, hover, loading, error, etc.)
- [ ] Contrast ratios pass WCAG
- [ ] Touch targets adequate
- [ ] Responsive behavior defined

---

## What's Next

In the tutorial, you'll generate and refine visuals for your own specifications, working through the design loop until you have polished, validated prototypes.

---

**[Continue to Tutorial: Create Your Visuals →](tutorial-15.md)**

---

[← Back to Lesson 1](lesson-01-making-it-visible.md) | [Back to Module Overview](module-15-visual-design-overview.md)
