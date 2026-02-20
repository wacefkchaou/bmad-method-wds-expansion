# Google Stitch

**Category:** AI UI Design & Code Generation
**Purpose:** Generate production-quality UI designs with real HTML/CSS code from text prompts or wireframes
**Website:** https://stitch.withgoogle.com/
**API:** Google Stitch API (via Google Cloud)
**MCP Servers:** Multiple available (see Installation)
**Requires:** Google Cloud account, Stitch API enabled

---

## What It Is

Google Stitch is a free AI UI design tool from Google Labs that generates complete UI designs with working HTML/CSS code. Unlike image generators that produce pictures of interfaces, Stitch produces real, editable code you can use directly.

**Used in WDS for:**
1. **Production mockups** - Generate HTML/CSS layouts from page specifications
2. **Wireframe digitization** - Upload hand-drawn sketches or Excalidraw wireframes and get coded UI
3. **Design iteration** - Quickly generate multiple layout variants with real code
4. **Figma export** - Generated designs can be exported to Figma with Auto Layout

**Output:** HTML/CSS code + visual preview, optionally exported to Figma.

---

## Capabilities

### What Stitch Does Well
- Generates complete HTML/CSS from text descriptions
- Converts wireframe images/sketches into coded UI
- Produces real, readable text (not garbled like image generators)
- Supports design tokens (colors, fonts, spacing)
- Exports to Figma with proper Auto Layout structure
- Creates responsive layouts
- Handles multiple design variants from one prompt

### Limitations
- Requires Google Cloud account and API access
- Generation limits: 350 standard (Flash) + 50 experimental (Pro) per month
- Does not generate JavaScript/interactivity
- Photo/image assets are placeholder only
- May not perfectly match complex custom layouts

---

## How It Compares

| Feature | Stitch | Nano Banana | Excalidraw | Figma |
|---------|--------|-------------|------------|-------|
| Output type | HTML/CSS code | Image (PNG) | Editable drawing | Design file |
| Text rendering | Real, readable | Garbled | Hand-drawn/typed | Perfect |
| Editable by user | Yes (code) | No (regenerate) | Yes (drag/draw) | Yes (design tool) |
| Layout accuracy | High | Approximate | Manual | Perfect |
| Speed | Fast | Fast | Manual | Manual |
| Best for | Production mockups | Image assets | Wireframes | Final polish |

**WDS recommended workflow:**
1. **Excalidraw** - Sketch and iterate on layout (editable, fast)
2. **Nano Banana** - Generate image assets (hero photos, card images, placeholders)
3. **Stitch** - Generate production HTML/CSS from approved wireframes

---

## Installation

### Option 1: Stitch MCP Server (Kargatharaakash)

Full-featured MCP server with 9 tools for the complete Stitch workflow.

**GitHub:** https://github.com/Kargatharaakash/stitch-mcp

**Tools provided:**
- `generate_screen_from_text` - Generate UI from text description
- `generate_screen_from_image` - Generate UI from wireframe/sketch image
- `list_projects` - List all Stitch projects
- `get_project` - Get project details
- `list_screens` - List screens in a project
- `get_screen` - Get screen details with HTML/CSS
- `export_to_figma` - Export design to Figma
- `update_screen` - Modify existing screen
- `delete_screen` - Remove a screen

**Install:**
```bash
# Clone and install
git clone https://github.com/Kargatharaakash/stitch-mcp.git
cd stitch-mcp
npm install

# Add to Claude Code
claude mcp add stitch -s user -- node /path/to/stitch-mcp/index.js
```

### Option 2: Stitch MCP Server (davideast)

Lightweight CLI-focused MCP server for pulling Stitch designs into development.

**GitHub:** https://github.com/davideast/stitch-mcp

**Tools provided:**
- `list_projects` - List projects
- `get_project` - Get project with screens
- `get_screen` - Get screen HTML/CSS

**Install:**
```bash
npx @anthropic-ai/claude-code mcp add stitch -- npx stitch-mcp
```

### Google Cloud Setup

Both MCP servers require Google Cloud authentication:

1. **Install Google Cloud SDK:**
   ```bash
   # Windows
   winget install Google.CloudSDK

   # macOS
   brew install google-cloud-sdk
   ```

2. **Authenticate:**
   ```bash
   gcloud auth application-default login
   ```

3. **Enable Stitch API:**
   ```bash
   gcloud services enable stitch.googleapis.com --project=YOUR_PROJECT_ID
   ```

4. **Restart Claude Code** to pick up the new MCP tools.

### Verify

```bash
claude mcp list
```

You should see:
```
stitch: ... - Connected
```

---

## Usage

### Generate from Text Description

Give Stitch a description of what you want:

```
"Generate a signup form with email and password fields,
a blue primary button labeled 'Create Account',
and a link to login below. Mobile-first, Inter font,
primary color #0066FF."
```

### Generate from Wireframe Image

Upload a wireframe (hand-drawn sketch, Excalidraw export, or digital wireframe) and Stitch converts it to coded UI.

```
"Convert this wireframe into a responsive HTML/CSS page.
Use the layout structure from the image. Apply these tokens:
Font: Inter, Primary: #0066FF, Background: #FFFFFF."
```

### Key Options

| Option | Description |
|--------|-------------|
| Text prompt | Describe the UI you want |
| Image input | Upload wireframe/sketch for conversion |
| Design tokens | Specify colors, fonts, spacing |
| Export format | HTML/CSS or Figma |

---

## WDS Workflows

### Visual Design (Phase 5: From Wireframe to Mockup)

The recommended pipeline for page design:

1. **Wireframe in Excalidraw** - Sketch layout, iterate freely
2. **Export wireframe** as PNG/SVG
3. **Generate with Stitch** - Upload wireframe + design tokens + page spec
4. **Review HTML/CSS** in browser
5. **Refine** - Adjust code or regenerate with updated prompt
6. **Export to Figma** if pixel-level refinement needed

**Recommended settings for page mockups:**
- Include design tokens (colors, fonts, spacing) in prompt
- Reference page specification for content and structure
- Start with mobile viewport, then generate desktop variant

### Asset Integration

Stitch generates the HTML/CSS structure. Combine with:
- **Nano Banana** images for hero photos, card images, seasonal visuals
- **Real brand assets** for logos, icons
- **Design system tokens** for consistent styling

---

## Best Practices

### DO

1. **Include design tokens in prompts** - Colors, fonts, spacing for consistent output
2. **Start from wireframes** - Upload Excalidraw exports for better layout accuracy
3. **Reference page specs** - Include key content (headlines, CTAs) in prompts
4. **Review in browser** - Always preview generated HTML/CSS live
5. **Iterate incrementally** - Refine specific sections rather than regenerating everything

### DON'T

1. **Don't expect production-ready code** - Generated code needs cleanup
2. **Don't skip wireframing** - Text-only prompts produce generic layouts
3. **Don't include too much detail** - Focus on structure and key content
4. **Don't forget responsive** - Specify mobile-first or desktop-first

---

## Troubleshooting

### API authentication fails

**Fix:** Run `gcloud auth application-default login` and follow browser authentication flow.

### Generation limits reached

**Standard (Flash):** 350 generations/month
**Experimental (Pro):** 50 generations/month

**Fix:** Wait for monthly reset, or create additional Google Cloud projects.

### MCP server not showing up

**Fix:** Restart Claude Code. Check `claude mcp list` for connection status.

### Generated layout doesn't match wireframe

**Fix:** Simplify the wireframe. Use clear section boundaries. Add text labels for key areas.

---

## Resources

- Stitch website: https://stitch.withgoogle.com/
- Stitch MCP (full): https://github.com/Kargatharaakash/stitch-mcp
- Stitch MCP (CLI): https://github.com/davideast/stitch-mcp
- Google Cloud SDK: https://cloud.google.com/sdk/docs/install

---

[Back to Tools](wds-tools-guide.md)
